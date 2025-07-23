<template>
  <div class="about">
    <h1 class="title">关于本站</h1>
    <div class="about-content" style="grid-template-columns: 3fr 2fr">
      <!-- 介绍 -->
      <div class="about-item hello">
        <span class="text1">你好，很高兴认识你👋</span>
        <span class="text2 title2">我是 Quisper</span>
        <span class="text3">是一名 喜欢尝试新东西的 学习者</span>
      </div>
      <!-- 追求 -->
      <div class="about-item pursuit">
        <span class="tip">追求</span>
        <span class="title2">源于</span>
        <span class="title2">热爱而去开发</span>
        <span class="title2">优秀的作品</span>
      </div>
    </div>
    <!-- 心路历程 -->
    <div class="about-content" style="display: flex">
      <div class="about-item">
        <span class="tip">心路历程</span>
        <span class="title2">为什么建站？</span>
        <p class="text">
          创建这个站的时候，想要就是能够有一个自己能够<strong>积累知识</strong>、<strong>积累兴趣</strong>的地方。和他人分享，会让这些成为<strong>积累和沉淀</strong>。如果能够帮助到更多的人，帮助更多人解决问题，那一定是非常棒的事情。
        </p>
        <p class="text">
          这里大多都是<strong>技术向</strong>的文章，可能不太会有很多人看，权当是做个自我记录吧。当然，如果某篇文章能够帮助到你，那我也是很开心的。
        </p>
        <p class="text">
          这些就是创造这个小站的本意，<strong>也是我分享生活的方式</strong>。有幸能和你相遇在这里，相信我们能共同留下一段美好记忆。
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
  // 当前页面未使用 JS 数据逻辑，script 可删除
</script>

<style lang="scss" scoped>
  .about {
    .title {
      font-size: 2.4rem;
      text-align: center;
      border: none;
    }

    .about-content {
      display: grid;
      grid-template-columns: auto auto;
      gap: 20px;
      margin-bottom: 20px;

      @media (max-width: 768px) {
        display: flex;
        flex-direction: column;
      }

      .about-item {
        position: relative;
        display: flex;
        flex-direction: column;
        width: 100%;
        padding: 1.2rem 2rem;
        border-radius: 12px;
        background-color: var(--main-card-background);
        border: 1px solid var(--main-card-border);
        box-shadow: 0 8px 12px -4px var(--main-border-shadow);
        overflow: hidden;

        .tip {
          font-size: 14px;
          opacity: 0.8;
          margin-bottom: 12px;
        }

        .title2 {
          font-size: 36px;
          font-weight: bold;
          margin-right: 4rem;
        }

        .text {
          font-size: 18px;
          margin: 0.6rem 0;
        }

        &.hello {
          justify-content: center;
          padding: 2rem;
          color: #fff;
          background-image: linear-gradient(120deg, #5b27ff 0%, #00d4ff 100%);
          background-size: 200% 200%;
          animation: gradientFlow 6s ease infinite;

          .title2 {
            line-height: 2;
          }
        }

        &.pursuit {
          .title2 {
            line-height: 1.2;

            &:last-child {
              display: inline-block;
              background-size: 100% 100%;
              background-clip: text;
              -webkit-background-clip: text;
              -webkit-text-fill-color: transparent;
              background-repeat: no-repeat;
              background-image: linear-gradient(45deg, #fa7671 50%, #f45f7f);
            }
          }
        }
      }

      &:last-child {
        margin-bottom: 0;
      }
    }
  }
</style>