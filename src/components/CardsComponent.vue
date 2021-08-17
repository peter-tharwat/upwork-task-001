<template>
  <div class="w-100 d-flex justify-content-center " >
    <div class="card" v-for="(mainType , index) in orders" v-bind:key="mainType.id">
      <div class="card-body px-1" >
        <div class="w-100 d-flex py-4 px-4 card-title">
          {{index}}
        </div>
        <div class=" px-4 d-flex py-3" v-for="order in mainType" v-bind:key="order.id">
          <div class="entry-card shadow rounded-2  w-100 d-flex">
            <div class="d-flex justify-content-end w-100 pt-3 px-4">
              <div class="dropdown">
                <span class="d-inline-block times-close dropdown-opener" >
                  <span></span>
                  <span></span>
                  <span></span>
                </span>
                <div class="dropdown-menu d-none">
                  <ul class="px-0 m-0">
                    <li><a href="#">Edit</a></li>
                    <li><a href="#">Show</a></li>
                    <li><a href="#" @click="cancelOrder(order.id)">Cancel</a></li>
                  </ul>
                </div>
              </div>
            </div>
            <div class="w-100 d-flex pt-4 pb-3 px-4 row justify-content-between border-bottom">
              <div class="d-flex w-50">
                <img :src="order.orderImage" class="task-image">
              </div>
              <div class="d-flex justify-content-start w-50 ">
                <div class="w-100 d-flex text-end">
                  <div class="d-inline-block w-100 pb-2">
                    <span class="d-inline-block badge  font-10 px-3 py-1" :class="order.orderBadgeClass">{{order.orderType}}</span>
                  </div>
                  <div class="d-inline-block font-11 w-100 pb-2">
                   {{order.date}}
                  </div>
                   <div class="d-inline-block font-11 w-100 pb-2">
                   {{order.interval}} <span class="opacity-25">|</span> <strong>{{order.currency}} {{order.price}}</strong>
                  </div>
                </div>
              </div>
            </div>
            <div class="w-100 d-flex" >
              <div class="w-50 px-4 py-4 font-12">
                <a href="#">View Order</a>
              </div>
              <div class="w-50 d-flex justify-content-end px-3 py-2">
                <img :src="order.avatarUrl" class="avatar-img">
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>
<!--     <div class="card">
      <div class="card-body">
        
      </div>
    </div> -->
   
  </div>
</template>
<style scoped>
.card-title{
  font-weight: bold;
}
.card-body .entry-card .times-close{
  cursor: pointer;
}
.card-body .entry-card .times-close span{
width: 4px;
height: 4px;
display: inline-block;
margin: 0px 1px ;
opacity: .6;
border-radius: 50%;
background: var(--main-body-color);
}
.card-body .entry-card{
  background: var(--main-entry-card-bg);
}
.card-body *{
font-size: 14px;
}
</style>
<script >
  export default {
    name: 'CardsComponent',
    data:function(){
      return {
        orders:{
          "New Orders":[
                {
                  id:1,
                  orderType:"New Order",
                  orderBadgeClass:"badge-warning",
                  date:"5 Days Ago",
                  interval:20 +" hrs",
                  price:85,
                  currency:"$",
                  orderImage:"/images/image.png",
                  avatarUrl:"/images/avatar.png"
                },
                {
                  id:2,
                  orderType:"New Order",
                  orderBadgeClass:"badge-warning",
                  date:"5 Days Ago",
                  interval:20 +" hrs",
                  price:85,
                  currency:"$",
                  orderImage:"/images/image.png",
                  avatarUrl:"/images/avatar.png"
                },
                {
                  id:3,
                  orderType:"New Order",
                  orderBadgeClass:"badge-warning",
                  date:"5 Days Ago",
                  interval:20 +" hrs",
                  price:85,
                  currency:"$",
                  orderImage:"/images/image.png",
                  avatarUrl:"/images/avatar.png"
                }
          ],
          "Under Processing":[
                {
                  id:4,
                  orderType:"Processing",
                  orderBadgeClass:"badge-info",
                  date:"5 Days Ago",
                  interval:20 +" hrs",
                  price:85,
                  currency:"$",
                  orderImage:"/images/image.png",
                  avatarUrl:"/images/avatar.png"
                },
                {
                  id:5,
                  orderType:"Processing",
                  orderBadgeClass:"badge-info",
                  date:"5 Days Ago",
                  interval:20 +" hrs",
                  price:85,
                  currency:"$",
                  orderImage:"/images/image.png",
                  avatarUrl:"/images/avatar.png"
                },
                {
                  id:6,
                  orderType:"Processing",
                  orderBadgeClass:"badge-info",
                  date:"5 Days Ago",
                  interval:20 +" hrs",
                  price:85,
                  currency:"$",
                  orderImage:"/images/image.png",
                  avatarUrl:"/images/avatar.png"
                }
          ],
          "Finished":[
                {
                  id:7,
                  orderType:"Finished",
                  orderBadgeClass:"badge-success",
                  date:"5 Days Ago",
                  interval:20 +" hrs",
                  price:85,
                  currency:"$",
                  orderImage:"/images/image.png",
                  avatarUrl:"/images/avatar.png"
                },
                {
                  id:8,
                  orderType:"Finished",
                  orderBadgeClass:"badge-success",
                  date:"5 Days Ago",
                  interval:20 +" hrs",
                  price:85,
                  currency:"$",
                  orderImage:"/images/image.png",
                  avatarUrl:"/images/avatar.png"
                },
          ],
          "Pending":[
                {
                  id:10,
                  orderType:"Pending",
                  orderBadgeClass:"badge-warning",
                  date:"5 Days Ago",
                  interval:20 +" hrs",
                  price:85,
                  currency:"$",
                  orderImage:"/images/image.png",
                  avatarUrl:"/images/avatar.png"
                },
          
          ],

        }
      }
    },
    methods:{
      cancelOrder:function(cardId){
        var result = confirm("Want to cancel order?");
        if (result) {
            alert("Hay Laravel Please Cancel the Order Number : "+cardId);
        }else{
            alert("Oh , You was about to cancel your order by mistake !");
        }
      }

    }
  }
</script>