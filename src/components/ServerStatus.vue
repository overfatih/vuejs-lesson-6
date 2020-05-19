<template>
    <div class="col-xs-12 col-sm-6">
        <p :style= " onAir ? { backgroundColor : 'green', color: 'white' }: { backgroundColor : 'red', }" >{{message}} </p>
        <button v-if="!onAir" @click="getServerStatus" >Güncelle</button>
      </div>
</template>
<script>
export default {
    data() {
        return {
            message     : "Sunucu Bilginizi Almak İçin Aşağıdaki Butona Basınız!",
            onAir       : false,
            messageText : 
            {
                wait    : "Sunucu Bilgisi bekleniyor",
                ok      : "Sunucu Bilgisi Güncel",
                error   : "Sunucu Bilgisi güncel değil!!"
            }
        }
    },
    watch: {
        onAir: function(value){
            this.message = value ? this.messageText.ok : this.messageText.error;
            /*sunucuya bağanıp bilgi çelirek onAir true/false olabilir*/
        }  
    },
    methods: {
        getServerStatus: function(){
            const vm = this;
            /*clearTimeout(myTimer1, myTimer2, myTimer3, myTimer4, myTimer5);*/
            this.message= this.messageText.wait;
            setTimeout(function(){ 
                vm.message += " . ";
                console.log("a");
            },1000);
            setTimeout(function(){ 
                vm.message += " . ";
                console.log("a");
            },2000);
            setTimeout(function(){ 
                vm.message += " .";
                console.log("a");
            },3000);
           setTimeout(function(){ vm.onAir=true; },4000);
           setTimeout(function(){ vm.onAir=false; },10000);
            

            
        }
        
    },
}
</script>
<style scoped>

</style>