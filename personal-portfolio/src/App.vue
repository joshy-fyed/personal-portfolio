<script setup lang="ts">
import { Download, Link, Message } from '@element-plus/icons-vue'
import {
  ElCol,
  ElText,
  ElContainer,
  ElMain,
  ElSpace,
  ElRow,
  ElCard,
  ElTimeline,
  ElTimelineItem,
  ElTag,
  ElDivider,
  ElButton,
} from 'element-plus'

const openExternal = (url: string) => {
  window.open(url, '_blank')
}

const openEmail = (email: string) => {
  window.location.href = `mailto:${email}`
}
</script>

<template>
  <ElContainer>
    <ElMain class="main-content">
      <!-- Hero Section -->
      <ElRow justify="center" class="section hero-section">
        <ElCol :xs="22" :sm="20" :md="18" :lg="14" :xl="10">
          <ElSpace direction="vertical" alignment="start" class="hero-content">
            <ElText class="hero-title">Joshua Visayan</ElText>
            <ElText class="hero-subtitle">Frontend Developer</ElText>
            <ElText type="info" class="hero-description">
              Building sleek, high-performance web experiences that turn complex ideas into
              intuitive, engaging interfaces. With a focus on accessibility, speed, and clean
              architecture, I create frontend solutions that users love and teams trust.
            </ElText>
            <ElSpace wrap class="hero-buttons">
              <ElButton
                class="hero-button"
                :icon="Link"
                plain
                @click="openExternal('https://github.com/yourusername')"
              >
                GitHub
              </ElButton>
              <ElButton
                class="hero-button"
                :icon="Link"
                plain
                @click="openExternal('https://linkedin.com/in/yourusername')"
              >
                LinkedIn
              </ElButton>
              <ElButton
                class="hero-button"
                :icon="Message"
                plain
                @click="openEmail('your.email@example.com')"
              >
                Email
              </ElButton>
              <ElButton
                class="hero-button"
                plain
                :icon="Download"
                @click="openExternal('/path-to-resume.pdf')"
              >
                Resume
              </ElButton>
            </ElSpace>
          </ElSpace>
        </ElCol>
      </ElRow>

      <!-- Work Experience Section -->
      <ElRow justify="center" class="section">
        <ElCol :xs="22" :sm="20" :md="18" :lg="14" :xl="10">
          <ElText class="section-title">Work Experience</ElText>
          <ElTimeline>
            <ElTimelineItem>
              <ElSpace direction="vertical" alignment="start" fill>
                <div class="timeline-header">
                  <ElSpace class="timeline-title-wrapper" wrap>
                    <ElText class="job-title">Software Engineer</ElText>
                    <ElTag type="success">Current</ElTag>
                  </ElSpace>
                  <ElText type="info" class="job-date">Feb 2024 - Present</ElText>
                </div>
                <ElText class="company-name">Mobile Internet Technology - Tokyo, Japan</ElText>
                <ElText type="info" class="job-description">
                  Working across frontend and backend development to modernize enterprise systems.
                  Played a key role in rebuilding a legacy POS management system, improving
                  performance, maintainability, and overall user experience. Collaborated closely
                  with a small team to deliver production-ready solutions on a tight timeline.
                </ElText>
                <ElSpace wrap class="tech-tags">
                  <ElTag size="large" type="info">Vue 3</ElTag>
                  <ElTag size="large" type="info">Go Lang</ElTag>
                  <ElTag size="large" type="info">TypeScript</ElTag>
                  <ElTag size="large" type="info">Element Plus</ElTag>
                  <ElTag size="large" type="info">Vite</ElTag>
                </ElSpace>
              </ElSpace>
            </ElTimelineItem>

            <ElTimelineItem>
              <ElSpace direction="vertical" alignment="start" fill>
                <div class="timeline-header">
                  <ElSpace class="timeline-title-wrapper" wrap>
                    <ElText class="job-title">WordPress Website Technician</ElText>
                  </ElSpace>
                  <ElText type="info" class="job-date">Jan 2023 - Jul 2023</ElText>
                </div>
                <ElText class="company-name">Sites at Scale - Dumaguete, Philippines</ElText>
                <ElText type="info" class="job-description">
                  Focused on building and maintaining high-volume client websites. Delivered custom
                  pages, improved responsiveness, and handled troubleshooting across multiple
                  WordPress projects, including e-commerce and VIP client requests.
                </ElText>
                <ElSpace wrap class="tech-tags">
                  <ElTag size="large" type="info">WordPress</ElTag>
                  <ElTag size="large" type="info">WPBakery</ElTag>
                  <ElTag size="large" type="info">Elementor</ElTag>
                  <ElTag size="large" type="info">WooCommerce</ElTag>
                  <ElTag size="large" type="info">PHP</ElTag>
                </ElSpace>
              </ElSpace>
            </ElTimelineItem>
          </ElTimeline>
        </ElCol>
      </ElRow>

      <!-- Skills Section -->
      <ElRow justify="center" class="section">
        <ElCol :xs="22" :sm="20" :md="18" :lg="14" :xl="10">
          <ElText class="section-title">Skills</ElText>
          <ElSpace wrap class="skills-container">
            <ElTag size="large" round type="info">Vue</ElTag>
            <ElTag size="large" round type="info">Go</ElTag>
            <ElTag size="large" round type="info">TypeScript</ElTag>
            <ElTag size="large" round type="info">SQL</ElTag>
            <ElTag size="large" round type="info">Docker</ElTag>
            <ElTag size="large" round type="info">Flutter</ElTag>
          </ElSpace>
        </ElCol>
      </ElRow>

      <!-- Projects Section -->
      <ElRow justify="center" class="section">
        <ElCol :xs="22" :sm="20" :md="18" :lg="14" :xl="10">
          <ElText class="section-title">Projects</ElText>
          <ElText class="projects-placeholder">
            Under construction... More projects coming soon!
          </ElText>
        </ElCol>
      </ElRow>
    </ElMain>
  </ElContainer>
</template>

<style scoped>
/* Base styles - Mobile first */
.main-content {
  padding: 0;
}

.el-text:not(.el-text--info) {
  color: white;
}

.section {
  padding: 1.25rem 0 2.5rem;
}

.hero-section {
  padding-top: 1.25rem;
  padding-bottom: 3rem;
}

/* Hero Section */
.hero-content {
  align-items: flex-start;
  width: 100%;
}

.hero-title {
  font-weight: 700;
  font-size: clamp(1.75rem, 5vw, 2.5rem);
  line-height: 1.2;
}

.hero-subtitle {
  font-size: clamp(1rem, 3vw, 1.2rem);
}

.hero-description {
  max-width: 100%;
  line-height: 1.6;
  font-size: clamp(0.875rem, 2vw, 1rem);
  margin-top: 0.5rem;
}

.hero-buttons {
  margin-top: 1rem;
}

.hero-button {
  font-family: 'Inter', sans-serif;
}

/* Section Titles */
.section-title {
  display: block;
  margin-bottom: 1.5rem;
  font-weight: 700;
  font-size: clamp(1.5rem, 4vw, 2rem);
  line-height: 1.2;
}

/* Timeline */
.timeline-header {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  width: 100%;
}

.timeline-title-wrapper {
  flex-wrap: wrap;
}

.job-title {
  font-weight: 700;
  font-size: clamp(1.125rem, 3vw, 1.5rem);
  line-height: 1.3;
}

.job-date {
  font-size: clamp(0.875rem, 2vw, 1rem);
}

.company-name {
  font-size: clamp(0.9rem, 2.5vw, 1.1rem);
  color: var(--el-text-color-regular);
  margin-top: 0.25rem;
}

.job-description {
  font-size: clamp(0.8rem, 2vw, 0.9rem);
  line-height: 1.6;
  padding-top: 0.5rem;
  text-align: justify;
}

.tech-tags {
  margin-top: 0.5rem;
}

/* Skills Section */
.skills-container {
  width: 100%;
}

/* Projects Section */
.projects-placeholder {
  font-size: clamp(0.875rem, 2vw, 1rem);
}

/* Tablet styles (768px+) */
@media (min-width: 768px) {
  .section {
    padding: 1.5rem 0 3rem;
  }

  .hero-section {
    padding-top: 1.5rem;
    padding-bottom: 3.75rem;
  }

  .hero-buttons {
    margin-top: 1.25rem;
  }

  .section-title {
    margin-bottom: 1.875rem;
  }

  .timeline-header {
    flex-direction: row;
    justify-content: space-between;
    align-items: flex-start;
  }

  .job-date {
    white-space: nowrap;
    margin-left: 1rem;
  }

  .tech-tags {
    margin-top: 0.75rem;
  }
}

/* Desktop styles (1024px+) */
@media (min-width: 1024px) {
  .section {
    padding: 1.25rem 0 3.75rem;
  }

  .hero-section {
    padding-top: 1.25rem;
    padding-bottom: 3.75rem;
  }

  .hero-description {
    max-width: 37.5rem;
  }

  .section-title {
    margin-bottom: 1.875rem;
  }

  .tech-tags {
    margin-top: 0.5rem;
  }
}
</style>
