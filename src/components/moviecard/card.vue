<template>
  <!--<div class="card">-->
    <!--<div class="card-img">-->
      <!--<img  v-lazy="data.images? data.images : null" class="img">-->
    <!--</div>-->
    <!--<div class="card-content">-->
      <!--<div class="desc">{{data.desc}}</div>-->
      <!--<div class="card-content-bottom">-->
        <!--<div class="who">{{data.who}}</div>-->
        <!--<div class="time">2017-12-33</div>-->
      <!--</div>-->
    <!--</div>-->
  <!--</div>-->
  <div class="card">
    <span class="info">
      <em>{{data.scope}}</em>
      <!--<a class="btn-trans" data-evt="index/movieBuy/9" href="?tmp=showcinemas&amp;movieid=336923">预告</a>-->
    </span>
    <a class="item ma-no" href="/movie/78608?_v_=yes" data-evt="index/moviehotList/4">
      <img class="J_ImgLoad" width="61" height="84" v-bind:src="data.logo">
      <div class="cont">
        <h4>
          <span>{{data.title}}</span>
          <span class="movie-tag">{{data.type}}</span>
        </h4>
        <p class="desc">{{data.desc}}</p>
        <p class="status">{{data.country}}</p>
        <p class="status">{{data.release}}</p>
      </div>
    </a>
  </div>
</template>

<script>
  export default {
    name: 'v-card',
    props: {
      data: {
        type: Object
      }
    }
  };
</script>
<!--<style lang="stylus" rel="stylesheet/stylus">-->
  <!--@import "card.styl";-->
<!--</style>-->
<style>
  .card {
    min-width: 320px;
    display: list-item;
    text-align: -webkit-match-parent;
  }
  .info {
    width: auto;
    float: right;
    padding: 10px 10px 0 0;
    text-align: right;
  }
  .info em {
    font-style: normal;
    display: block;
    color: #ff9a00;
    font-size: 20px;
    line-height: 24px;
    white-space: nowrap;
    font-weight: 400;
    text-decoration: none;
    background: 0;
    vertical-align: middle;
  }
  .card .item {
    display: block;
    padding: 8px 10px 4px;
    border-bottom: 1px solid #d6d6d6;
    min-height: 90px;
  }
  a {
    outline: 0;
    text-decoration: none;
  }
  a:-webkit-any-link {
    color: -webkit-link;
    text-decoration: underline;
    cursor: auto;
  }
  .card img {
    float: left;
  }

  .lazy img {
    background: #c1c1c1 url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAMAAAAp4XiDAAAAwFBMV…mytghhgpB+Cgix7I1gjStOqq8c5jhkmLqiJ0McuoXq6j92ZWbxiZAstgAAAABJRU5ErkJggg==) no-repeat center center;
  }
  img {
    border: 0;
    vertical-align: top;
    width: 61px;
    height: 84px;
  }
  /*.cont {*/
    /*margin: 0 65px 4px 68px;*/
  /*}*/
  div {
    display: block;
  }
  /*h1, h2, h3, h4, h5, h6 {*/
    /*font-size: 100%;*/
    /*font-weight: 400;*/
  /*}*/
  body, h1, h2, h3, h4, h5, h6, p, ul, ol, figure, textarea, input, button, select {
    margin: 0;
  }
  .card h4 {
    padding: 0px;
    font-size: 16px;
    padding: 2px 0 4px;
    color: #000;
    max-height: 45px;
    overflow: hidden;
    line-height: 1.2;
  }
  /*h4 {*/
    /*display: block;*/
    /*-webkit-margin-before: 1.33em;*/
    /*-webkit-margin-after: 1.33em;*/
    /*-webkit-margin-start: 0px;*/
    /*-webkit-margin-end: 0px;*/
    /*font-weight: bold;*/
  /*}*/
  .movie-tag-3d {
    background: #49d95d;
  }
  .movie-tag {
    display: inline-block;
    padding: 0 4px 2px;
    font-size: 11px;
    background: #2895db;
    border-radius: 3px;
    margin: 2px 0 0 4px;
    color: #fff;
    text-align: center;
    vertical-align: top;
    line-height: 17px;
    height: 14px;
  }
  .card .cont p {
    padding: 1px 0;
    margin: 0px;
    color: #666;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    text-decoration: none;
    cursor: auto;
  }
  p {
    display: block;
    -webkit-margin-before: 1em;
    -webkit-margin-after: 1em;
    -webkit-margin-start: 0px;
    -webkit-margin-end: 0px;
  }
  .card .status {
    font-size: 10px;
    padding-top: 2px;
  }
  .desc {
    margin: 0 0 2px 0;
    padding: 0;
    color: #666;
    height: 16px;
    font-size: 14px;
  }
  a:link,a:visited{
    text-decoration:none;  /*超链接无下划线*/
  }
  .card .info em:after {
    content: '分';
    font-size: 12px;
    padding-left: 2px;
  }
  .btn-trans {
    font-size: 13px;
    padding: 4px 17px;
    background-color: transparent;
    border-radius: 4px;
    border: 1px solid #e54847;
    color: #e54847 !important;

    display: inline-block;
    vertical-align: top;
    white-space: nowrap;
    margin-top: 20px;
  }
</style>
