<script setup lang="js">
defineProps({
  bookList: {
    type: Array,
    default: () => {
      return []
    },
  },
})
</script>

<template>
  <div class="FeishuShelf">
    <div class="sidebar">
      <div class="feishu-icon">
        <svg width="1em" height="1em" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-icon="LarkLogoColorful"><path d="m12.924 12.803.056-.054c.038-.034.076-.072.11-.11l.077-.076.23-.227 1.334-1.319.335-.331c.063-.063.13-.123.195-.183a7.777 7.777 0 0 1 1.823-1.24 7.607 7.607 0 0 1 1.014-.4 13.177 13.177 0 0 0-2.5-5.013 1.203 1.203 0 0 0-.94-.448h-9.65c-.173 0-.246.224-.107.325a28.23 28.23 0 0 1 8 9.098c.007-.006.016-.013.023-.022Z" fill="#00D6B9" /><path d="M9.097 21.299a13.258 13.258 0 0 0 11.821-7.247c-.113.22-.243.43-.378.625a5.219 5.219 0 0 1-1.098 1.152 3.777 3.777 0 0 1-.262.185 5.117 5.117 0 0 1-.353.218 4.643 4.643 0 0 1-.726.331 5.317 5.317 0 0 1-1.883.312 5.892 5.892 0 0 1-.524-.031 6.509 6.509 0 0 1-.729-.126c-.06-.016-.12-.029-.18-.044-.167-.044-.33-.092-.495-.14-.082-.024-.164-.046-.246-.072-.123-.038-.246-.072-.366-.11l-.3-.095-.284-.094-.192-.067a4.955 4.955 0 0 1-.233-.082 3.452 3.452 0 0 1-.168-.06c-.11-.04-.22-.079-.328-.12l-.189-.072-.252-.098c-.089-.035-.18-.07-.269-.107l-.173-.07c-.073-.028-.142-.06-.215-.088l-.164-.07-.17-.075-.148-.066-.136-.06-.139-.063a90.183 90.183 0 0 1-.142-.066 4.808 4.808 0 0 0-.18-.083c-.063-.028-.123-.06-.186-.088a5.697 5.697 0 0 1-.198-.098 27.762 27.762 0 0 1-8.067-5.969.18.18 0 0 0-.313.123l.007 9.21c0 .4.198.779.533 1a13.177 13.177 0 0 0 7.325 2.205Z" fill="#3370FF" /><path d="M23.732 9.295a7.55 7.55 0 0 0-3.35-.776 7.521 7.521 0 0 0-2.284.35c-.054.016-.107.035-.158.05a8.297 8.297 0 0 0-.855.35 7.14 7.14 0 0 0-.552.297 6.716 6.716 0 0 0-.533.347c-.123.089-.243.18-.363.275-.13.104-.252.211-.375.321-.067.06-.13.123-.196.184l-.334.328-1.338 1.321-.23.228-.076.075c-.038.038-.076.073-.11.11l-.057.054a1.914 1.914 0 0 1-.085.08c-.032.028-.063.06-.095.088a13.286 13.286 0 0 1-2.748 1.946c.06.028.12.057.18.082l.142.066c.044.022.091.041.139.063l.135.06.149.067.17.075.164.07c.073.031.142.06.215.088.056.025.116.047.173.07.088.034.177.072.268.107.085.031.168.066.253.098l.189.072c.11.041.218.082.328.12.057.019.11.041.167.06.08.028.155.053.234.082l.192.066.284.095.3.095c.123.037.243.075.366.11l.246.072c.164.048.331.095.495.14.06.015.12.03.18.043.114.029.227.05.34.07.13.022.26.04.389.057a5.815 5.815 0 0 0 .994.019 5.172 5.172 0 0 0 1.413-.3 5.405 5.405 0 0 0 .726-.334c.06-.035.122-.07.182-.108a7.96 7.96 0 0 0 .432-.297 5.362 5.362 0 0 0 .577-.517 5.285 5.285 0 0 0 .37-.429 5.797 5.797 0 0 0 .527-.827l.13-.258 1.166-2.325-.003.006a7.391 7.391 0 0 1 1.527-2.186Z" fill="#133C9A" /></svg>
        飞书云文档
      </div>

      <div class="siderbar-menu">
        <ul>
          <li class="active">
            <span>
              <svg width="18" height="18" viewBox="0 0 24 24"><path d="M9.5 22a1 1 0 001-1v-4a1 1 0 011-1h1a1 1 0 011 1v4a1 1 0 001 1H20a2 2 0 002-2V10a2 2 0 00-.75-1.56l-8-5.94a2 2 0 00-2.5 0l-8 5.94A2 2 0 002 10v10a2 2 0 002 2h5.5z" /></svg>
            </span>
            主页
          </li>
          <li>
            <span>
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M7 15a1 1 0 100 2h10a1 1 0 100-2H7z" fill="#2B2F36" /><path d="M1.5 5a2 2 0 012-2h4.78a4 4 0 011.4.26l2.64.99a4 4 0 001.4.25h6.78a2 2 0 012 2V19a2 2 0 01-2 2h-17a2 2 0 01-2-2V5zm19 14V7h-17v12h17z" fill="#2B2F36" /></svg>
            </span>
            我的空间
          </li>
          <li>
            <span>
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M8.5 5a2.5 2.5 0 100 5 2.5 2.5 0 000-5zM4 7.5a4.5 4.5 0 119 0 4.5 4.5 0 01-9 0zM5.83 15a3.37 3.37 0 00-3.33 3.4V20h12v-1.6c0-1.9-1.51-3.4-3.33-3.4H5.82zM.5 18.4c0-2.98 2.39-5.4 5.33-5.4h5.33a5.37 5.37 0 015.34 5.4V20a2 2 0 01-2 2h-12a2 2 0 01-2-2v-1.6zm22 2.6h-4.13v-2h3.13v-.6c0-1-.84-1.9-2-1.9h-1.31a5.46 5.46 0 00-.98-2h2.29c2.21 0 4 1.75 4 3.9V20c.03.54-.49 1.02-1 1zm-6-11a1 1 0 111 1 1 1 0 01-1-1zm1-3a3 3 0 000 6 3 3 0 000-6z" fill="#2B2F36" /></svg>
            </span>
            共享空间
          </li>
          <li>
            <span>
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M2.5 2.5a1 1 0 011-1h13a5 5 0 015 5v15a1 1 0 01-1 1h-13a5 5 0 01-5-5v-15zm2 1V7h9a3 3 0 013 3v10.5h3v-14a3 3 0 00-3-3h-12zm0 9h5a2 2 0 012 2v6h3V10a1 1 0 00-1-1h-9v3.5zm0 2v3a3 3 0 003 3h2v-6h-5z" fill="#2B2F36" /></svg>
            </span>
            知识库
          </li>
          <li>
            <span>
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M1.18 8.41a1.5 1.5 0 01.62-2.03l7.9-4.2a1.5 1.5 0 012.03.62l.29.53-5.9 1.34a2.5 2.5 0 00-1.88 3l2.6 11.38L1.17 8.4z" fill="#2B2F36" /><path d="M6.84 5.78a1.5 1.5 0 00-1.13 1.8l2.73 11.96c.06.26.19.5.36.68V7.55a2.5 2.5 0 012.5-2.5h6.34l-.05-.18a1.5 1.5 0 00-1.79-1.13L6.84 5.78z" fill="#2B2F36" /><path d="M10.2 7.9a1.5 1.5 0 011.5-1.5h8.85a1.5 1.5 0 011.5 1.5v12.6a1.5 1.5 0 01-1.5 1.5H11.7a1.5 1.5 0 01-1.5-1.5V7.9z" fill="#2B2F36" /></svg>
            </span>
            词典
          </li>
          <li>
            <span>
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M12 3.69l2.44 3.78a3 3 0 001.74 1.27l4.35 1.18-2.84 3.54a3 3 0 00-.66 2.03l.23 4.54-4.18-1.62a3 3 0 00-2.16 0l-4.18 1.61.23-4.53a3 3 0 00-.66-2.03L3.47 9.92l4.35-1.18a3 3 0 001.74-1.27L12 3.69zm1.26-1.74a1.5 1.5 0 00-2.52 0L7.88 6.4a1 1 0 01-.58.42L2.2 8.19a1.5 1.5 0 00-.78 2.38l3.32 4.14a1 1 0 01.22.68l-.27 5.3a1.5 1.5 0 002.04 1.48l4.9-1.9a1 1 0 01.72 0l4.9 1.9a1.5 1.5 0 002.04-1.48l-.27-5.3a1 1 0 01.21-.68l3.33-4.14a1.5 1.5 0 00-.78-2.38L16.7 6.8a1 1 0 01-.58-.42l-2.86-4.44z" fill="#2B2F36" /></svg>
            </span>
            收藏
          </li>
          <li>
            <span>
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M10 16a1 1 0 100 2h4a1 1 0 100-2h-4z" fill="#2B2F36" /><path d="M10 2a2 2 0 00-2 2H3a1 1 0 000 2h1v14a2 2 0 002 2h12a2 2 0 002-2V6h1a1 1 0 100-2h-5a2 2 0 00-2-2h-4zM6 20V6h12v14H6z" fill="#2B2F36" /></svg>
            </span>
            回收站
          </li>
        </ul>
      </div>

      <div class="sidbar-bottom">
        <div class="divider" />
        <div class="save">
          <span>
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M11.44 16.2a.38.38 0 00-.37.38v1.58c0 .2.16.37.37.37h1.59a.38.38 0 00.37-.37v-1.59a.38.38 0 00-.38-.37h-1.58zm3.83.38c0-.21.16-.38.37-.38h1.58c.21 0 .38.17.38.38v1.58a.38.38 0 01-.38.37h-1.58a.38.38 0 01-.37-.37v-1.59z" fill="#2B2F36" /><path d="M17.8 2.67H6.2a.93.93 0 00-.9.71L2.7 14.11a.93.93 0 00-.03.26v6.03c0 .52.41.93.93.93h16.8a.93.93 0 00.93-.93v-6.07a.93.93 0 00-.05-.32L18.7 3.38a.93.93 0 00-.91-.71zm1.26 10.7H4.94l2.1-8.74h9.92l2.1 8.74zm-14.4 6.06V15.3h14.67v4.13H4.67z" fill="#2B2F36" /></svg>
          </span>
          存储管理
        </div>
      </div>
    </div>

    <div class="right">
      <div class="search">
        <div class="search-bar">
          <img class="search-icon" src="https://img.icons8.com/ios-glyphs/30/000000/search--v1.png" alt="搜索图标">
          <input type="text" placeholder="搜索">
          <svg width="1em" height="1em" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-icon="AdvancedActivedOutlined"><path d="M1 4a1 1 0 0 1 1-1h20a1 1 0 1 1 0 2H2a1 1 0 0 1-1-1Zm3 8a1 1 0 0 1 1-1h14a1 1 0 1 1 0 2H5a1 1 0 0 1-1-1Zm4 7a1 1 0 1 0 0 2h8a1 1 0 1 0 0-2H8Z" fill="currentColor" /></svg>
        </div>
        <div class="icons">
          <svg width="1em" height="1em" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-icon="WikilinkOutlined"><path d="M13 7.855A3.502 3.502 0 0 0 12 1a3.5 3.5 0 0 0-1 6.855v2.271a4.002 4.002 0 0 0-2.82 5.063l-1.7 1.425a3.5 3.5 0 1 0 1.258 1.555l1.51-1.266A3.987 3.987 0 0 0 12 18a3.987 3.987 0 0 0 2.752-1.097l1.51 1.267a3.5 3.5 0 1 0 1.258-1.555l-1.7-1.427A4.002 4.002 0 0 0 13 10.125v-2.27ZM12 6a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3Zm0 10a2 2 0 1 1 0-4 2 2 0 0 1 0 4Zm-6 3.5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0ZM19.5 21a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3Z" fill="currentColor" /></svg>
          <svg width="1em" height="1em" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-icon="EfficiencyOutlined"><path d="M3.113 11.357a7.065 7.065 0 0 0 4.807 6.116.17.17 0 0 1 .107.107l.554 1.663a1.84 1.84 0 0 0 1.744 1.257h3.35c.791 0 1.494-.506 1.744-1.257l.554-1.663a.17.17 0 0 1 .107-.107 7.065 7.065 0 0 0 4.807-6.116L21 10a9 9 0 1 0-18 0l.113 1.357Zm10.963 5.59-.518 1.553h-3.117l-.517-1.552a2.17 2.17 0 0 0-1.372-1.372 5.065 5.065 0 0 1-3.446-4.385L5 9.921a7 7 0 0 1 14 0l-.106 1.27a5.065 5.065 0 0 1-3.446 4.385 2.17 2.17 0 0 0-1.372 1.372ZM10 21.5a1 1 0 1 0 0 2h4a1 1 0 1 0 0-2h-4Z" fill="currentColor" /></svg>
          <svg width="1em" height="1em" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-icon="HelpdeskOutlined"><path d="M6 9a6 6 0 1 1 12 0v6.5a5.502 5.502 0 0 1-4.155 5.334A1.5 1.5 0 0 0 12.5 20h-2a1.5 1.5 0 0 0 0 3h2a7.5 7.5 0 0 0 7.5-7.5v.5h.5a2 2 0 0 0 2-2v-3a2 2 0 0 0-2-2H20A8 8 0 1 0 4 9h-.5a2 2 0 0 0-2 2v3a2 2 0 0 0 2 2H6V9Z" fill="currentColor" /></svg>
          <svg width="1em" height="1em" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-icon="DialpadOutlined"><path d="M4 6a2 2 0 1 0 0-4 2 2 0 0 0 0 4Zm0 8a2 2 0 1 0 0-4 2 2 0 0 0 0 4Zm2 6a2 2 0 1 1-4 0 2 2 0 0 1 4 0Zm6-14a2 2 0 1 0 0-4 2 2 0 0 0 0 4Zm2 6a2 2 0 1 1-4 0 2 2 0 0 1 4 0Zm-2 10a2 2 0 1 0 0-4 2 2 0 0 0 0 4Zm8-16a2 2 0 1 0 0-4 2 2 0 0 0 0 4Zm2 6a2 2 0 1 1-4 0 2 2 0 0 1 4 0Zm-2 10a2 2 0 1 0 0-4 2 2 0 0 0 0 4Z" fill="currentColor" /></svg>
          <img src="https://img.icons8.com/ios-filled/50/000000/user.png" alt="用户头像">
        </div>
      </div>

      <div class="header">
        <div class="header-title">
          主页
        </div>
        <div class="header-btn-group">
          <button class="header-btn">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" class="explorer__button-template-icon" style="width: 14px; height: 14px;"><path d="M14 13.5a6.5 6.5 0 11-13 0 6.5 6.5 0 0113 0z" fill="#5B65F5" /><path d="M10.65 2.85a2 2 0 012.45-1.42l7.7 2.07a2 2 0 011.42 2.45l-2.07 7.7a2 2 0 01-2.45 1.41L10 13a2 2 0 01-1.41-2.45l2.06-7.7z" fill="#FCCA03" /><path d="M13.89 10.3a1 1 0 011.73 0l5.77 10a1 1 0 01-.87 1.5H9a1 1 0 01-.87-1.5l5.77-10z" fill="#F54A45" /></svg>
            模版库
          </button>
          <button class="header-btn">
            上传
            <svg width="1em" height="1em" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-icon="DownBoldOutlined"><path d="m3.414 7.086-.707.707a1 1 0 0 0 0 1.414l7.778 7.778a2 2 0 0 0 2.829 0l7.778-7.778a1 1 0 0 0 0-1.414l-.707-.707a1 1 0 0 0-1.415 0l-7.07 7.07-7.072-7.07a1 1 0 0 0-1.414 0Z" fill="currentColor" /></svg>
          </button>
          <button class="header-btn new">
            新建
            <svg width="1em" height="1em" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-icon="DownBoldOutlined"><path d="m3.414 7.086-.707.707a1 1 0 0 0 0 1.414l7.778 7.778a2 2 0 0 0 2.829 0l7.778-7.778a1 1 0 0 0 0-1.414l-.707-.707a1 1 0 0 0-1.415 0l-7.07 7.07-7.072-7.07a1 1 0 0 0-1.414 0Z" fill="currentColor" /></svg>
          </button>
        </div>
      </div>

      <div class="scroll-area">
        <div class="banner">
          <div class="banner-left">
            <div class="banner-title">
              职场利器：一站式玩转多维表格
            </div>
            <div class="sub-title">
              快速学习多维表格玩法，轻松掌控全盘业务，创造无限可能
            </div>

            <div class="banner-btn-group">
              <div class="banner-btn">
                🙋 新手入门
                <svg width="16" height="16" viewBox="0 0 12 12"><path d="M4.15 2.85a.5.5 0 11.7-.7L8.71 6 4.85 9.85a.5.5 0 01-.7-.7L7.29 6 4.15 2.85z" fill="#7E8791" fill-rule="nonzero" /></svg>
              </div>
              <div class="banner-btn">
                🎬 视频课程
                <svg width="16" height="16" viewBox="0 0 12 12"><path d="M4.15 2.85a.5.5 0 11.7-.7L8.71 6 4.85 9.85a.5.5 0 01-.7-.7L7.29 6 4.15 2.85z" fill="#7E8791" fill-rule="nonzero" /></svg>
              </div>
              <div class="banner-btn">
                🥇 客户案例
                <svg width="16" height="16" viewBox="0 0 12 12"><path d="M4.15 2.85a.5.5 0 11.7-.7L8.71 6 4.85 9.85a.5.5 0 01-.7-.7L7.29 6 4.15 2.85z" fill="#7E8791" fill-rule="nonzero" /></svg>
              </div>
              <div class="banner-btn">
                📖 查询页面上新
                <svg width="16" height="16" viewBox="0 0 12 12"><path d="M4.15 2.85a.5.5 0 11.7-.7L8.71 6 4.85 9.85a.5.5 0 01-.7-.7L7.29 6 4.15 2.85z" fill="#7E8791" fill-rule="nonzero" /></svg>
              </div>
            </div>
          </div>

          <div class="banner-right">
            <img src="https://p3-zeus.byteimg.com/img/tos-cn-i-tv0gyzr5fi/450d675e29344d34adee556585dd0a47.png~tplv-tv0gyzr5fi-image.image" class="sc-hatPLa sc-hzbjEY kHBzHO gSCHTw">
            <span size="20" class="sc-eALafw sc-jcndOL huDVyW eUBRqC" style="top: 24px; right: 24px;"><svg width="20" height="20" viewBox="0 0 20 20"><g fill="none" fill-rule="evenodd"><circle cx="10" cy="10" r="10" fill="#c4c7cb" /><path fill="#fff" d="M6.64 5.58L10 8.94l3.36-3.36c.2-.2.51-.2.7 0l.36.35c.2.2.2.52 0 .71L11.06 10l3.36 3.36c.2.2.2.51 0 .7l-.35.36a.5.5 0 01-.71 0L10 11.06l-3.36 3.36a.5.5 0 01-.7 0l-.36-.35a.5.5 0 010-.71L8.94 10 5.58 6.64a.5.5 0 010-.7l.35-.36c.2-.2.52-.2.71 0z" /></g></svg></span>
          </div>
        </div>

        <div class="latest">
          <div class="title">
            最近
          </div>
          <div class="table-title">
            <div class="book-title">
              所有类型
              <svg width="1em" height="1em" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-icon="DownBoldOutlined"><path d="m3.414 7.086-.707.707a1 1 0 0 0 0 1.414l7.778 7.778a2 2 0 0 0 2.829 0l7.778-7.778a1 1 0 0 0 0-1.414l-.707-.707a1 1 0 0 0-1.415 0l-7.07 7.07-7.072-7.07a1 1 0 0 0-1.414 0Z" fill="currentColor" /></svg>
            </div>
            <div class="author">
              不限归属
              <svg width="1em" height="1em" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-icon="DownBoldOutlined"><path d="m3.414 7.086-.707.707a1 1 0 0 0 0 1.414l7.778 7.778a2 2 0 0 0 2.829 0l7.778-7.778a1 1 0 0 0 0-1.414l-.707-.707a1 1 0 0 0-1.415 0l-7.07 7.07-7.072-7.07a1 1 0 0 0-1.414 0Z" fill="currentColor" /></svg>
            </div>
            <div class="time">
              最近打开
              <svg width="1em" height="1em" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-icon="DownBoldOutlined"><path d="m3.414 7.086-.707.707a1 1 0 0 0 0 1.414l7.778 7.778a2 2 0 0 0 2.829 0l7.778-7.778a1 1 0 0 0 0-1.414l-.707-.707a1 1 0 0 0-1.415 0l-7.07 7.07-7.072-7.07a1 1 0 0 0-1.414 0Z" fill="currentColor" /></svg>
            </div>
            <div class="opt">
              <svg width="24" height="24" viewBox="0 0 24 24"><g fill="none" fill-rule="evenodd"><rect width="24" height="24" rx="2" /><path fill="#7E8791" d="M19 18a1 1 0 01-1 1H6a1 1 0 01-1-1V6a1 1 0 011-1h12a1 1 0 011 1v12zm-12.5-.5h4.75v-4.75H6.5v4.75zm11-4.75h-4.75v4.75h4.75v-4.75zm0-1.5V6.5h-4.75v4.75h4.75zM11.25 6.5H6.5v4.75h4.75V6.5z" /></g></svg>
            </div>
          </div>

          <div v-for="item in bookList" :key="item.title" class="book-item">
            <div class="book-title">
              <img :src="item.img">
              {{ item.title }}
            </div>
            <div class="author">
              {{ item.author }}
            </div>
            <div class="time">
              5月31日 19:36
            </div>
            <div class="opt">
              <span class="universe-icon"><svg width="1em" height="1em" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-icon="MoreOutlined"><path d="M5.5 11.75a1.75 1.75 0 1 1-3.5 0 1.75 1.75 0 0 1 3.5 0Zm8.225 0a1.75 1.75 0 1 1-3.5 0 1.75 1.75 0 0 1 3.5 0Zm8.275 0a1.75 1.75 0 1 1-3.5 0 1.75 1.75 0 0 1 3.5 0Z" fill="currentColor" /></svg></span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import "FeishuShelf.css";
</style>
