<script setup>
import lawyerProfile from '@/assets/lawyer-profile.avif'

// 需求 7：更新後的經歷清單
const experiences = [
  '伯衡法律事務所 受僱律師',
  '吉訟法律事務所 實習律師',
  '萬海航運股份有限公司 法務風險管理師',
  '臺灣宜蘭地方法院 民事庭書記官',
  '華泓國際運輸股份有限公司 法務專員'
]

</script>

<template>
  <div class="bg-navy py-5" data-aos="fade-down">
    <div class="container text-center">
      <i class="bi bi-person-badge-fill fs-2 mb-2" style="color:#b8860b;"></i>
      <h1 class="text-white fw-bold">關於律師</h1>
      <p style="color:rgba(255,255,255,.7);">精準法律判斷，穩健風險控管</p>
    </div>
  </div>

  <section class="py-5">
    <div class="container">
      <div class="row align-items-center g-5">
        <div class="col-lg-4 text-center" data-aos="zoom-in">
          <div class="rounded-4 shadow-lg overflow-hidden mb-3 mx-auto" style="aspect-ratio:3/4;max-width:300px;border:3px solid rgba(184,134,11,.35);">
            <img :src="lawyerProfile" alt="林仁修律師" style="width:100%;height:100%;object-fit:cover;object-position:top;" />
          </div>
          <h4 class="fw-bold mb-0" style="color:#1a2a6c;">林仁修 律師</h4>
          <p class="text-muted small">Attorney at Law｜修律</p>
        </div>
        
        <div class="col-lg-8" data-aos="fade-left">
          <h2 class="section-title">個人簡介</h2>
          <p style="line-height:1.9;" class="text-muted fw-bold">
            林仁修律師致力於清晰、直接的法律服務，幫助每一位面對法律問題的當事人找到最有利的出路。
          </p>
          <p style="line-height:1.9;" class="text-muted">
            秉持「精準法律判斷，穩健風險控管」的核心理念，林律師深信法律服務不應只是冷冰冰的條文與程序，而應讓每一位委任人都能真正理解自己的處境。
          </p>

          <div class="mt-4">
            <h5 class="fw-bold mb-3" style="color:#1a2a6c;">經歷</h5>
            <ul class="list-unstyled">
              <li v-for="exp in experiences" :key="exp" class="d-flex align-items-center gap-2 mb-2 text-muted">
                <i class="bi bi-check2-square" style="color:#b8860b;"></i>{{ exp }}
              </li>
            </ul>
          </div>

        </div>
      </div>
    </div>
  </section>
  </template>
