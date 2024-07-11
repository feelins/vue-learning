<template>
    <h1>CSS Box</h1>
    <img src="../images/box-model-1.png" height="300px">

    <div class="main">
        CSS Box-Model Property
    </div>

    <div class="gfg">
        <div class="gfg1">
            GeeksforGeeks
        </div>

        <div class="gfg2">
            A computer science portal for geeks
        </div>
    </div>
    <img src="../images/layout_html.gif">
    <div class="margin4">top</div>
    <p class="margin4">
        margin: 40px 100px 120px 80px; <br>
        top margin = 40px<br>
    right margin = 100px<br>
    bottom margin = 120px<br>
    left margin = 80px</p>
    <div class="margin4">bottom</div>

    <div class="margin3">top</div>
    <p class="margin3">
        margin: 40px 100px 120px;  <br>
        top = 40px<br>
right and left = 100px<br>
bottom = 120px</p>
    <div class="margin3">bottom</div>

    <div class="margin2">top</div>
    <p class="margin2">
        margin: 40px 100px;  <br>
        top and bottom = 40px<br>
        right and left = 100px<br></p>
    <div class="margin2">bottom</div>
    
</template>

<style lang="scss">
    h1,
    h2 {
        color: green;
        text-align: center;
    }
    .main {
        font-size: 36px;
        font-weight: bold;
        Text-align: center;
        margin-top: 100px;
    }
    
    .gfg {
        margin-left: 60px;
        border: 50px solid #009900;
        width: 300px;
        height: 200px;
        text-align: center;
        padding: 50px;
        margin-bottom: 100px;
    }
    
    .gfg1 {
        font-size: 42px;
        font-weight: bold;
        color: #009900;
        margin-top: 60px;
        background-color: #c5c5db;
    }
    
    .gfg2 {
        font-size: 18px;
        font-weight: bold;
        background-color: #c5c5db;
    }

    div.margin4 {
        background-color: #c5c5db;
    }
    p.margin4 {
        margin: 40px 100px 120px 80px;
        background-color: #c5c555;
    }

    div.margin3 {
        background-color: #de3523;
    }
    p.margin3 {
        margin: 40px 100px 120px;
        background-color: #c5c555;
    }

    div.margin2 {
        background-color: #de3923;
    }
    p.margin2 {
        margin: 40px 100px;
        background-color: #c9c555;
    }
</style>