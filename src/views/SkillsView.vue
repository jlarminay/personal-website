<script setup>
import { ref } from 'vue'
import InlineSvg from 'vue-inline-svg'

let icons = ref([
  'vuejs',
  'python',
  'godot',
  'raspberrypi',
  'digitalocean',
  'docker',
  'nginx',
  'nodejs',
  'php',
  'postgresql',
  'tailwindcss',
])
</script>

<template>
  <section class="justify-center md:flex">
    <div class="order-2 p-5 md:w-[650px]">
      <div class="mb-10">
        <h1>Some skills and stuff.</h1>
        <ul class="hidden">
          <li>
            Learn some Infrastructure as Code (IaC) tools like Terraform and
            Ansible.
          </li>
          <li>Learning mobile development with Flutter.</li>
          <li>I want to make more games with Godot.</li>
        </ul>
      </div>

      <div class="mb-5">
        <h2>My favorite languages and tools.</h2>
        <div class="mb-7 flex flex-wrap justify-start">
          <div
            v-for="(icon, index) in icons"
            :key="index"
            class="group relative m-3 w-[75px]"
          >
            <InlineSvg
              :src="'/images/logos/' + icon + '.svg'"
              :alt="icon"
              :title="icon"
              class="absolute top-0 z-10 h-full w-full blur-none transition-all group-hover:blur-sm"
            />
            <InlineSvg
              :src="'/images/logos/' + icon + '.svg'"
              :alt="icon"
              :title="icon"
              class="relative top-0 z-20 h-full w-full"
            />
          </div>
        </div>
      </div>

      <div>
        <h2>What I'm doing next.</h2>
        <ul>
          <li>
            Learn some Infrastructure as Code (IaC) tools like Terraform and
            Ansible.
          </li>
          <li>Learning mobile development with Flutter.</li>
          <li>I want to make more games with Godot.</li>
        </ul>
      </div>
    </div>
    <div class="order-1 mx-auto w-[400px] max-w-[80%] p-10 md:w-[350px]">
      <img src="/images/josh-point.png" class="w-full" />
    </div>
  </section>
</template>

<style scoped lang="postcss"></style>
