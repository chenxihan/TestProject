<script setup lang="ts">
import { Monitor, Setting, Tools } from '@element-plus/icons-vue'

const features = [
  {
    title: 'Vue 3',
    description: '使用 Composition API 和单文件组件组织业务代码。',
    icon: Monitor,
  },
  {
    title: 'Vite',
    description: '提供快速开发服务器、热更新和生产构建。',
    icon: Tools,
  },
  {
    title: 'Element Plus',
    description: '已接入组件库和图标库，可直接开发后台界面。',
    icon: Setting,
  },
]
</script>

<template>
  <el-config-provider>
    <main class="app-shell">
      <section class="intro">
        <div>
          <p class="eyebrow">Vue3 + Vite + TypeScript + Element Plus</p>
          <h1>项目框架已就绪</h1>
          <p class="summary">这是一个可直接扩展的前端工程起点，包含 TypeScript、路径别名和 Element Plus 全局注册。</p>
        </div>
        <el-button type="primary" size="large" :icon="Tools">开始开发</el-button>
      </section>

      <section class="feature-grid">
        <el-card v-for="feature in features" :key="feature.title" shadow="never">
          <div class="feature-icon">
            <el-icon :size="24">
              <component :is="feature.icon" />
            </el-icon>
          </div>
          <h2>{{ feature.title }}</h2>
          <p>{{ feature.description }}</p>
        </el-card>
      </section>
    </main>
  </el-config-provider>
</template>
