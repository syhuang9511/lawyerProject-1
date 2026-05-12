<script setup>
const cases = [
  {
    category: '刑事辯護',
    title: '竊盜案件 - 成功爭取不起訴處分',
    description: '當事人遭指控涉嫌竊盜罪，林律師介入後發現證詞與事實不符，成功還原真相，檢察官最終裁定不起訴。'
  },
  {
    category: '家事案件',
    title: '離婚訴訟 - 成功爭取子女監護權',
    description: '面對高衝突的離婚訴訟，林律師協助當事人蒐集對子女最有利的照顧事實，最終法院判歸當事人單獨監護。'
  },
  {
    category: '民事訴訟',
    title: '房屋租賃糾紛 - 成功追回押金與損害賠償',
    description: '屋主無故扣押高額押金不還，林律師透過法律途徑不僅追回全數押金，並額外爭取到延遲給付之利息。'
  },
  {
    category: '非訟事件',
    title: '遺產繼承 - 排除非法繼承權益',
    description: '處理複雜的家族遺產繼承，林律師透過代擬遺囑與法律分析，確保當事人的合法繼承份額不受侵害。'
  }
]
</script>

<template>
  <div class="cases-page">
    <section class="py-5 bg-navy text-white text-center">
      <div class="container py-4">
        <h1 class="display-5 fw-bold">成功案例</h1>
        <div class="divider-gold mx-auto my-3"></div>
        <p class="lead">辦案實績與成功經驗分享，用成果證明專業</p>
      </div>
    </section>

    <section class="py-5 bg-light-custom">
      <div class="container">
        <div class="row g-4">
          <div v-for="(item, index) in cases" :key="index" class="col-md-6">
            <div class="card h-100 border-0 shadow-sm p-4 card-hover">
              <div class="mb-2">
                <span class="badge" style="background-color: rgba(184, 134, 11, 0.1); color: #b8860b;">{{ item.category }}</span>
              </div>
              <h5 class="fw-bold mb-3" style="color: #1a2a6c;">{{ item.title }}</h5>
              <p class="text-muted small mb-0" style="line-height: 1.8;">
                {{ item.description }}
              </p>
            </div>
          </div>
        </div>

        <div class="mt-5 text-center">
          <p class="text-muted">法律案件涉及隱私，以上僅列出部分代表性案例，詳情歡迎預約諮詢。</p>
          <RouterLink to="/contact" class="btn btn-gold px-5 py-2 mt-2">
            <i class="bi bi-chat-text me-2"></i>我也要諮詢
          </RouterLink>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.card-hover {
  transition: all 0.3s ease;
  border-left: 4px solid transparent !important;
}
.card-hover:hover {
  transform: translateY(-5px);
  border-left: 4px solid #b8860b !important;
}
</style>