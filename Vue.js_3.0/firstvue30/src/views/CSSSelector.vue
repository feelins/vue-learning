<template>
    <p>Geeks</p>
    <p>Hello</p>
    <div class="red green-text">This is a div.</div>
    <div class="red">This is a div.</div>
    <span id="blue">This is a span.</span>
    <ul>
        <li class="red">This is Item1.</li>
        <li><a href="1.com">This is Item2.</a></li>
        <li><a href="1.com" target="_blank">This is Item3.</a></li>
    </ul>
    <h1>CSS Pseudo Elements</h1>
    <h1>Geeks For Geeks</h1>
    <h2>::first-line element</h2>

    <p class="first-line">
        This is a paragraph using first-line
        pseudo-element to style first line of
        the paragraph. Content in the first 
        line turns red and becomes bold.
    </p>
    <h1>Geeks For Geeks</h1>
    <h2>::first-letter element</h2>
    <p class="first-letter">
        This is a paragraph using first-letter
        pseudo-element to style first letter
        of the paragraph. first-letter element
        turned the first letter of this paragraph
        to red and made it bold.
    </p>
    <h1>Geeks For Geeks</h1>
    <h2>::before element</h2>

    <p class="before">
        This is a paragraph to which
        we added red color quotation
        marks using ::before element.
    </p>

    <h1>Geeks For Geeks</h1>
    <h2>::selection element</h2>

    <p>
        Content in this paragraph turns
        red with green background on selection.
    </p>

    <span>
        As this is not a paragraph, you can
        notice red background and green text on
        selection.
    </span>

    <h1>Geeks For Geeks</h1>
    <h2>:hover Pseudo-class</h2>
    <div class="box">
        My color changes if you hover over me!
    </div>

    <h1>Geeks For Geeks</h1>
    <h2>:focus Pseudo-class</h2>
    <form>
        <label for="username">Username:</label>
        <input type="text" name="username" 
               placeholder="Enter your username" />
        <br>

        <label for="emailid">Email-Id:</label>
        <input type="email" name="emailid" 
               placeholder="Enter your email-id" />

        <label for="Password">Password:</label>
        <input type="password" name="Password" 
               placeholder="Enter your password" />
    </form>

    <p>GeeksforGeeks</p>
    <div>General sibling selector property</div>
    <p>GeeksforGeeks</p>
    <span>
        <div>child div content</div>
        <p>G4G</p>
    </span>
    
</template>

<style lang="scss">
    h1,
    h2 {
        color: green;
        text-align: center;
    }
    body {
        background-color: whitesmoke;
        color: green;
        font-size: large;
        text-align: center;
    }
        
    p.first-line::first-line {
        color: Red;
        font-weight: bold;
    }

    p.first-letter::first-letter {
        color: Red;
        font-size: 30px;
        font-weight: bold;
    }

    p.before::before {
        content: '"';
        color: red;
        font-size: 30px;
    }

    ul {
        width: 400px;
    }

    ul li::marker {
        color: red;
        font-size: 30px;
    }

    .box {
        background-color: yellow;
        width: 300px;
        height: 200px;
        margin: auto;
        font-size: 40px;
        text-align: center;
    }

    .box:hover {
        background-color: orange;
    }

    p::selection {
        color: red;
        background-color: green;
        font-size: 30px;
    }
    
    ::selection {
        color: green;
        background-color: red;
        font-size: 30px;
    }

    // * {
    //     background:darkcyan;
    // }

    a[target] {
        background-color: yellow;
    }

    .red {
        background-color: red;
    }

    #blue {
        background-color: blue;
    }

    div.red.green-text {
        background-color: brown;
        color: greenyellow;
    }

    form{
        width: 300px;
        height: 200px;
        margin: 0 auto;
        text-align: center;
        line-height: 2rem;
    }
    
    label{
        width: 30%;
    }
    
    input{
        background-color: default;
        float: right;
    }
    
    input:focus{
        background-color:blueviolet;
    }

    div ~ p{
        color: #009900;
        font-size:32px;
        font-weight:bold;
        margin:0px;
        text-align:center;
    }
    div {
        text-align:center;
    }
</style>