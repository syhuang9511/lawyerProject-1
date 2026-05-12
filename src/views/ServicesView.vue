<script setup>
const services = [
  {
    icon: 'bi-person-check-fill',
    title: '各類民事案件',
    summary: '全程代理各類民事糾紛，從起訴策略規劃到強制執行，保障您的每一項民事權益。',
    details: [
      '侵權行為損害賠償（車禍、醫療糾紛）',
      '借貸、票據、債務不履行等金錢糾紛',
      '房屋買賣、租賃爭議',
      '假扣押、假處分、強制執行聲請',
    ],
  },
  {
    icon: 'bi-people-fill',
    title: '各類家事案件', // 需求 2：獨立分類
    summary: '細心處理家庭法律紛爭，在理性與感性間為您爭取最合理的權益。',
    details: [
      '離婚訴訟、協議離婚撰擬',
      '贍養費、扶養費請求',
      '子女監護權爭取與探視權安排',
      '收養程序法律諮詢、保護令聲請',
    ],
  },
  {
    icon: 'bi-shield-fill',
    title: '各類刑事案件',
    summary: '從偵查階段起全程陪同，制定最有力的辯護策略，守護您的自由與清白。',
    details: [
      '竊盜、賭博、恐嚇取財案件辯護', // 需求 5：更新內容
      '詐欺、背信、侵占等財產犯罪',
      '傷害、妨害自由、性侵害案件',
    ],
  },
  {
    icon: 'bi-building',
    title: '警局陪偵',
    summary: '收到警察傳票或遭約談，第一時間安排律師陪同到場，確保權益。',
    details: [
      '刑事案件偵查中陪同製作筆錄',
      '搜索扣押現場法律協助',
      '偵訊前完整行前說明與策略討論',
    ],
  },
  {
    icon: 'bi-file-earmark-text',
    title: '非訟事件',
    // 需求 3：修正為「非訟程序」
    summary: '不需要打官司也能解決的法律問題，透過非訟程序快速有效地達成目的。',
    details: [
      '代擬遺囑', // 需求 6：更新內容
      '本票裁定、支付命令聲請',
      '調解、仲裁程序代理',
    ],
  },
  {
    icon: 'bi-briefcase-fill',
    title: '法律顧問',
    summary: '為企業及個人提供長期法律諮詢服務，合約把關、風險預防。',
    details: [
      '商業合約起草、審閱、談判',
      '勞動合約、競業禁止條款審查',
      '定期法律風險評估與法律健診',
    ],
  },
]

// 確保保留委任服務流程的資料
const steps = [
  { icon: 'bi-telephone', label: '聯繫諮詢', desc: '電話、LINE 或填單，說明您的問題' },
  { icon: 'bi-file-earmark-text', label: '案情評估', desc: '分析法律爭點，說明策略與費用' },
  { icon: 'bi-pen', label: '簽約委任', desc: '確認委任範圍，透明計費無隱費' },
  { icon: 'bi-person-workspace', label: '全力執行', desc: '積極代理，定期回報案件進度' },
]
</script>

<template>
  <div class="bg-navy py-5 text-center" data-aos="fade-down">
    <div class="container">
      <i class="bi bi-grid-3x3-gap-fill fs-2 mb-2" style="color:#b8860b;"></i>
      <h1 class="text-white fw-bold">服務項目</h1>
      <p style="color:rgba(255,255,255,.7);" class="mb-0">精準法律判斷，穩健風險控管，為您打造最有利的解決方案</p>
    </div>
  </div>

  <section class="py-5 bg-light-custom">
    <div class="container">
      <div class="row g-4">
        <div v-for="(svc, i) in services" :key="svc.title" class="col-md-6 col-lg-4">
          <div class="card service-card h-100 p-4">
            <div class="d-flex align-items-center gap-3 mb-3">
              <div class="rounded-circle d-flex align-items-center justify-content-center flex-shrink-0" style="width:52px;height:52px;background:rgba(26,42,108,.08);">
                <i :class="['bi', svc.icon]" style="color:#1a2a6c;font-size:1.5rem;"></i>
              </div>
              <h5 class="fw-bold mb-0" style="color:#1a2a6c;">{{ svc.title }}</h5>
            </div>
            <p class="text-muted mb-3 small">{{ svc.summary }}</p>
            <ul class="list-unstyled mb-0">
              <li v-for="d in svc.details" :key="d" class="d-flex align-items-start gap-2 mb-2 small">
                <i class="bi bi-check-circle-fill mt-1 flex-shrink-0" style="color:#b8860b;"></i>
                <span>{{ d }}</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="py-5">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="fw-bold" style="color:#1a2a6c;">委任服務流程</h2>
        <div class="divider-gold"></div>
      </div>
      <div class="row g-4 text-center">
        <div v-for="(step, i) in steps" :key="step.label" class="col-sm-6 col-lg-3">
          <div class="mx-auto mb-3 rounded-circle d-flex align-items-center justify-content-center" style="width:72px;height:72px;background:#1a2a6c;color:#b8860b;font-size:1.8rem;">
            <i :class="['bi', step.icon]"></i>
          </div>
          <span class="badge mb-2" style="background:#b8860b;">Step {{ i + 1 }}</span>
          <h6 class="fw-bold" style="color:#1a2a6c;">{{ step.label }}</h6>
          <p class="small text-muted">{{ step.desc }}</p>
        </div>
      </div>
    </div>
  </section>
</template>