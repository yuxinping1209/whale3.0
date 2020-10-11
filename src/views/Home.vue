<template>
<div>
    <div class="topnav">
        <div class="logo">logo</div>
        <div class="menu">
            <span style="margin-right:20px;">菜单1</span>
            <span>菜单2</span>
        </div>
    </div>
    <div class="banner">
        <h1>轮子</h1>
        <h2>一个厉害的UI框架</h2>
        <p class="actions">
            <a>github</a>
            <a>开始</a>
        </p>
    </div>
</div>
</template>

<style lang="scss">
.topnav {
    border: 1px solid red;
    background: #efefef;
    display: flex;
    justify-content: space-between;

    .logo,
    .menu {
        margin: 20px 40px 20px 40px;
    }
}
</style>
