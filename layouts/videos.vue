<template>
<div>    
<main class="mainbox"> 
  <v-app class="Filter" >
         <v-chip-group active-class="blue white--text" v-model="selection" column class="list">
          <v-chip>All</v-chip>
          <v-chip>Music</v-chip>
          <v-chip>Live</v-chip>
          <v-chip>4k Fireplace</v-chip>
          <v-chip>Game Shows</v-chip>
          <v-chip>Ambient music</v-chip>
          <v-chip>Gaming</v-chip> 
          <v-chip>Recently uploaded</v-chip> 
          <v-chip>Never</v-chip>
          <v-chip>Gonna</v-chip> 
          <v-chip>Give</v-chip>
          <v-chip>You</v-chip>
          <v-chip>Up</v-chip>
          <v-chip>Amogus</v-chip>
          <v-chip>More old jokes</v-chip>
          <v-chip>2014 memes</v-chip>
          <v-chip>Meat, i'm dissapointed</v-chip>
        </v-chip-group>
    <v-card
      class="m-1"
      max-width="374" >
      <v-img height="250" src="https://i.redd.it/2s0m3gxfr5t61.jpg"></v-img>
   <v-card-title> Failures will soon take over </v-card-title>
      <v-card-text>
        <v-row class="mx-0">
          <div class="grey--text ms-1"> <img src="data:image/jpeg;base64,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" alt="" class="pfp">
          Steven He Enjoyer
          </div>
          <div class="time">3:13</div>
        </v-row>
      <v-row>
        <div class="grey--text ms-4" > 102M views · 1 day ago</div></v-row>
      </v-card-text>
    </v-card>

    <v-card class="m-2" max-width="374" >
      <v-img height="250" src="https://www.creatopy.com/blog/wp-content/uploads/2020/06/pewdiepie-youtube-thumbnail-font-1024x576.jpg"></v-img>
   <v-card-title> Tired of being rick rolled</v-card-title>
      <v-card-text>
        <v-row class="mx-0">
          <div class="grey--text ms-1"> <img src="https://yt3.ggpht.com/5oUY3tashyxfqsjO5SGhjT4dus8FkN9CsAHwXWISFrdPYii1FudD4ICtLfuCw6-THJsJbgoY=s176-c-k-c0x00ffffff-no-rj" alt="soma" class="pfp">
          Pewdiepie
          </div>
          <div class="time">3:13</div>
        </v-row>
      <v-row>
        <div class="grey--text ms-4" > 1B views · 2 days ago</div></v-row>
      </v-card-text>
    </v-card>

     <v-card class="b-1" max-width="374" >
      <v-img height="250" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSjjcOUqklbMXMpUNAu_BA9dCrEB0MzzzPiaQ&usqp=CAU"></v-img>
   <v-card-title> Times Pewdiepie got rick rolled </v-card-title>
      <v-card-text>
        <v-row class="mx-0">
          <div class="grey--text ms-1"> <img src="https://c.tenor.com/x8v1oNUOmg4AAAAC/rickroll-roll.gif" alt="soma" class="pfp">
          NotRickAstley
          </div>
          <div class="time">5:14</div>
        </v-row>
      <v-row>
        <div class="grey--text ms-4" > 178K views · 3 days ago</div></v-row>
      </v-card-text>
    </v-card>

      <v-card class="b-2" max-width="374" >
      <v-img height="250" src="https://cdn.britannica.com/s:800x450,c:crop/43/172743-138-545C299D/overview-Barack-Obama.jpg"></v-img>
   <v-card-title>Top 10 N words sequel</v-card-title>
      <v-card-text>
        <v-row class="mx-0">
          <div class="grey--text ms-1"> <img src="https://sun9-46.userapi.com/impg/97Rk_pHY6wr9umXu34_zId6KuLeQcJSyiBVQGg/4G1PL5kJj1s.jpg?size=453x604&quality=96&sign=56737366cc18ee55f803ccc8c68ce47e&type=album" alt="soma" class="pfp">
          Trippycoast</div>
          <div class="time">0:25</div>
        </v-row>
      <v-row>
        <div class="grey--text ms-4" > 1M views · 1 week ago</div></v-row>
      </v-card-text>
    </v-card>

      <v-card class="e-1" max-width="374" >
      <v-img height="250" src="https://c.tenor.com/x8v1oNUOmg4AAAAC/rickroll-roll.gif"></v-img>
   <v-card-title> Guide to not losing </v-card-title>
      <v-card-text>
        <v-row class="mx-0">
          <div class="grey--text ms-1"> <img src="https://c.tenor.com/x8v1oNUOmg4AAAAC/rickroll-roll.gif" alt="soma" class="pfp">
          NotRickAstley</div>
          <div class="time">3:13</div>
        </v-row>
      <v-row>
        <div class="grey--text ms-4" > 920k views · 3 weeks ago</div></v-row>
      </v-card-text>
    </v-card>

          <v-card class="e-2" max-width="374" >
      <v-img height="250" src="https://cdn.vox-cdn.com/thumbor/HVFBMHsTrpSpc2O9pdSYHIEDIlU=/1400x788/filters:format(jpeg)/cdn.vox-cdn.com/uploads/chorus_asset/file/10480483/acastro_180322_1777_youtube_0001.jpg"></v-img>
   <v-card-title> Youtube got rick rolled lol</v-card-title>
      <v-card-text>
        <v-row class="mx-0">
          <div class="grey--text ms-1"> <img src="https://c.tenor.com/x8v1oNUOmg4AAAAC/rickroll-roll.gif" alt="soma" class="pfp">
          NotRickAstley</div>
          <div class="time2">Enough time for you to waste</div>
        </v-row>
      <v-row>
        <div class="grey--text ms-4" > LMAO REKT views · 1 year ago</div></v-row>
      </v-card-text>
    </v-card>



    </v-app>
  </main>
</div>
</template>

<script>
export default {
  data: () => ({

selection: 0,
  })
}
</script>

<style scoped>

      .m-1 {
        background-color: rgb(255, 255, 255);
        color: gray;
        left: 300px;
        top: 40px;
   }
      .m-2 {
        background-color: rgb(255, 255, 255);
        color: rgb(133, 133, 133);
        left: 300px;
        top: 100px;
   }
      .b-1 {
        background-color: rgb(255, 255, 255);
        color: rgb(133, 133, 133);
        left: 730px;
        top: -689px;
   }
      .b-2 {
        background-color: rgb(255, 255, 255);
        color: rgb(133, 133, 133);
        left: 730px;
        top: -628px;
   }
      .e-1 {
        background-color: rgb(255, 255, 255);
        color: rgb(133, 133, 133);
        left: 1170px;
        top: -1420px;
   }
      .e-2 {
        background-color: rgb(255, 255, 255);
        color: rgb(133, 133, 133);
        left: 1170px;
        top: -1355px;
   }
      .mainbox {
        background-color: rgb(255, 255, 255);
        width: 1920px;
        height: 1000px;
        margin-top: 70px;
   }

      .Filter {
        background-color: white;
    }
      .pfp{
        border-radius: 50%;
        width: 30px;
        height: 30px;
    }
      .list {
        margin-left: 270px;
        font-size: 500px;
        color: white;
   }
      .time {
        font-size: .8em;
        position: absolute;
        transform: translate(317px, -80px);
        padding: 3px;
        padding-right: 10px;
        padding-left: 10px;
        border-radius: 3px;
        color: white;
        background-color: rgba(0, 0, 0, 0.733);
      }
      .time2 {
        font-size: .8em;
        position: absolute;
        transform: translate(-15px, -80px);
        padding: 3px;
        padding-right: 10px;
        padding-left: 10px;
        border-radius: 3px;
        color: white;
        background-color: rgba(0, 0, 0, 0.733);
      }


</style>