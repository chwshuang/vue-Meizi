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
      <em>8.9</em>
    </span>
    <a class="item ma-no" href="/movie/78608?_v_=yes" data-evt="index/moviehotList/4">
      <img class="J_ImgLoad" width="61" height="84" src="//p0.meituan.net/165.220/movie/e631df85c6cadddafc6792cd94fd14ad6081426.jpeg.webp">
      <div class="cont">
        <h4>
          <span>刺客信条</span>
          <span class="movie-tag">3D IMAX</span>
        </h4>
        <p class="desc">穿越黑科技，法鲨炫腹肌</p>
        <p class="status">本周五上映</p>
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
    padding: 10px 10px 12px;
    border-bottom: 1px solid #d6d6d6;
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
    padding: 4px 0 7px;
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
    padding: 3px 0;
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
    font-size: 12px;
    padding: 3px 0;
  }
  .desc {
    margin: 0;
    padding: 0;
    color: #666;
    height: 21px;
  }
  a:link,a:visited{
    text-decoration:none;  /*超链接无下划线*/
  }
  .card .info em:after {
    content: '分';
    font-size: 12px;
    padding-left: 2px;
  }
</style>
