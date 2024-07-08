<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div id="container">
      <div id="leftside" class="content">
        <h1>The Future</h1>
      </div>
      <div id="rightside" class="content">
        <h1>The Past</h1>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
  #container {
    height: 400px;
    background-color: chocolate;
    display: flex;
    justify-content:space-between;
    clip-path: circle(100%);
  }

  #rightside {
    color: white;
    background-color:darkgreen;
    
  }

  #leftside {
    background-color:bisque;
  }
</style>