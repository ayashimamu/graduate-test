<template>
  <div class="todolist">
      <p class="title">ToDo List</p>
      <input type="text" v-model="Text">
      <button class="add " @click="add" type="submit">追加</button>
       <div v-for="(value,index) in list" :key="index">
         <div class="list-item">
           <input type="text" v-model="value.ListText"/>
           <button class="update">更新</button>
           <button class="delete">削除</button>
         </div>
         </div>
  </div>
</template>
<script>
export default{
data(){
  return{
    list:[]
  }
},
methods:{
  add(){
    this.list.push({
    ListText:this.Text
  });
}
}
};


</script>

<style>
html, body, div, span, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
abbr, address, cite, code,
del, dfn, em, img, ins, kbd, q, samp,
small, strong, sub, sup, var,
b, i,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, figcaption, figure,
footer, header, hgroup, menu, nav, section, summary,
time, mark, audio, video {
    margin:0;
    padding:0;
    border:0;
    outline:0;
    font-size:100%;
    vertical-align:baseline;
    background:transparent;
}

body {
    line-height:1;
}

article,aside,details,figcaption,figure,
footer,header,hgroup,menu,nav,section {
    display:block;
}

nav ul {
    list-style:none;
}

blockquote, q {
    quotes:none;
}

blockquote:before, blockquote:after,
q:before, q:after {
    content:'';
    content:none;
}

a {
    margin:0;
    padding:0;
    font-size:100%;
    vertical-align:baseline;
    background:transparent;
}

/* change colours to suit your needs */
ins {
    background-color:#ff9;
    color:#000;
    text-decoration:none;
}

/* change colours to suit your needs */
mark {
    background-color:#ff9;
    color:#000;
    font-style:italic;
    font-weight:bold;
}

del {
    text-decoration: line-through;
}

abbr[title], dfn[title] {
    border-bottom:1px dotted;
    cursor:help;
}

table {
    border-collapse:collapse;
    border-spacing:0;
}

/* change border colour to suit your needs */

input, select {
  vertical-align:middle;
  width: 80%;
  height: 35px;
  border: 1px solid rgb(172, 172, 172);
  border-radius: 10px;
}

html {
  background-color: #320d97;
}
* {
  color: black;
  font-family: "Noto Sans JP";
}
.todolist{
  background: white;
  width: 50%;
  height: auto;
  padding: 30px;
  margin-top: 20%;
  margin-left: 25%;
}
.title{
  font-size: 24px;
  font-weight: 600;
  font-family: Serif;
}
input:focus{
  outline: none;
}
button{
 background: white;
 border-radius: 10px;
 padding: 7px 10px;
 margin-top: 20px;
}
button:focus{
  outline: none;
}
.add{
 background: white;
 color: rgb(214, 9, 214);
 border: 2px solid rgb(214, 9, 214);
 margin-left: 40px ;
}
.list-item{
  margin-top: 20px;
}
.update{
  color: rgb(248, 129, 17);
  border: 2px solid  rgb(248, 129, 17);
}
.delete{
  color: rgb(8, 255, 255);
  border: 2px solid rgb(8, 255, 255) ;
}
</style>
