<script setup lang="ts">
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
    <ElMain>
      <!-- Hero Section -->
      <ElRow justify="center" style="padding: 20px 0 60px 0">
        <ElCol :span="10">
          <ElSpace direction="vertical" style="align-items: flex-start">
            <ElText style="font-size: 1rem;">Frontend Developer</ElText>
            <ElText style="font-weight: 700; font-size: 2.5rem">Joshua Visayan</ElText>
            <ElText type="info" style="max-width: 600px"
              >Building sleek, high-performance web experiences that turn complex ideas into
              intuitive, engaging interfaces. With a focus on accessibility, speed, and clean
              architecture, I create frontend solutions that users love and teams trust.</ElText
            >
            <ElSpace wrap style="margin-top: 10px">
              <ElButton class="hero-button" plain @click="openExternal('https://github.com/yourusername')">
                GitHub
              </ElButton>
              <ElButton class="hero-button" plain @click="openExternal('https://linkedin.com/in/yourusername')">
                LinkedIn
              </ElButton>
              <ElButton class="hero-button" plain @click="openEmail('your.email@example.com')">
                Email
              </ElButton>
              <ElButton class="hero-button" plain @click="openExternal('/path-to-resume.pdf')">
                Resume
              </ElButton>
            </ElSpace>
          </ElSpace>
        </ElCol>
      </ElRow>

      <!-- What I Work With Section -->
      <ElRow justify="center" style="padding: 20px 0 60px 0">
        <ElCol :span="10">
          <ElText
            style="
              display: block;
              margin-bottom: 30px;
              font-weight: 700;
              font-size: 2rem;
            "
            >What I Work With</ElText
          >
          <ElSpace wrap>
            <ElTag size="large">Vue</ElTag>
            <ElTag size="large">Go</ElTag>
            <ElTag size="large">TypeScript</ElTag>
            <ElTag size="large">SQL</ElTag>
            <ElTag size="large">Docker</ElTag>
            <ElTag size="large">Flutter</ElTag>
          </ElSpace>
        </ElCol>
      </ElRow>

      <!-- Work Experience Section -->
      <ElRow justify="center" style="padding: 20px 0 60px 0">
        <ElCol :span="10">
          <ElText
            style="
              display: block;
              margin-bottom: 30px;
              font-weight: 700;
              font-size: 2rem;
            "
            >Work Experience</ElText
          >
          <ElTimeline>
            <ElTimelineItem timestamp="Feb 2024 - Present" placement="top">
              <ElCard>
                <template #header>
                  <ElSpace>
                    <ElText tag="b">Software Engineer</ElText>
                    <ElTag type="success">Current</ElTag>
                  </ElSpace>
                </template>
                <ElText tag="p" style="padding-bottom: 10px"
                  >Mobile Internet Technology - Tokyo, Japan</ElText
                >
                <ElText tag="p" type="info"
                  >Working across frontend and backend development to modernize enterprise systems.
                  Played a key role in rebuilding a legacy POS management system, improving
                  performance, maintainability, and overall user experience. Collaborated closely
                  with a small team to deliver production-ready solutions on a tight
                  timeline.</ElText
                >
                <ElSpace wrap style="margin-top: 10px">
                  <ElTag>Vue 3</ElTag>
                  <ElTag>Go Lang</ElTag>
                  <ElTag>TypeScript</ElTag>
                  <ElTag>Element Plus</ElTag>
                  <ElTag>Vite</ElTag>
                </ElSpace>
              </ElCard>
            </ElTimelineItem>

            <ElTimelineItem timestamp="Jan 2023 - Jul 2023" placement="top">
              <ElCard>
                <template #header>
                  <ElText tag="b">Website Technician (WordPress)</ElText>
                </template>
                <ElText tag="p" style="padding-bottom: 10px"
                  >Sites at Scale - Dumaguete, Philippines</ElText
                >
                <ElText tag="p" type="info"
                  >Focused on building and maintaining high-volume client websites. Delivered custom
                  pages, improved responsiveness, and handled troubleshooting across multiple
                  WordPress projects, including e-commerce and VIP client requests.</ElText
                >
                <ElSpace wrap style="margin-top: 10px">
                  <ElTag>WordPress</ElTag>
                  <ElTag>WPBakery</ElTag>
                  <ElTag>Elementor</ElTag>
                  <ElTag>WooCommerce</ElTag>
                  <ElTag>PHP</ElTag>
                </ElSpace>
              </ElCard>
            </ElTimelineItem>
          </ElTimeline>
        </ElCol>
      </ElRow>

      <!-- Projects Section -->
      <ElRow justify="center" style="padding: 20px 0 60px 0">
        <ElCol :span="10">
          <ElText
            style="
              display: block;
              margin-bottom: 30px;
              font-weight: 700;
              font-size: 2rem;
            "
            >Projects</ElText
          >
          <ElText>
            Under construction... More projects coming soon!
          </ElText>
        </ElCol>
      </ElRow>
    </ElMain>
  </ElContainer>
</template>

<style scoped>

.hero-button {
  font-family: 'Inter', sans-serif;
}
</style>
