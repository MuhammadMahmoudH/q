<template>
  <div>

    <ul>
      <li v-for="user in users" v-if="isdisplay">
        user: {{user.name}}, address: {{user.address}}, age: {{user.age}}, tel: {{user.tel}}
      </li>
    </ul>

    <br>
    favorites: <span v-for="favorit in favorites">{{favorit}}, </span> <br>
    <!--<input type="button" @click="isdisplay = !isdisplay" value="click me"/>-->
    <input type="button" @click="changeDisplay" value="click me"/>

  </div>
</template>

<script>

export default {
    data(){
        return{

            address:'El Haram',
            //one dimension array
            favorites:['Football','English Movies','Reading','Drawing'],
            //multi dimensions array
            users:[
                {name:'ahmed',address:'haram',age:21,tel:123456},
                {name:'mostafa',address:'fesal',age:23,tel:444333},
                {name:'hanafy',address:'maadi',age:32,tel:22323242}
            ],
            isdisplay: false
        }
    },
    methods:{
        changeDisplay(){
            this.isdisplay = !this.isdisplay
        }
    }
}
</script>

<style>

</style>
