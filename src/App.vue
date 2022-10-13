<template>
  <div class="scale-75" v-auto-animate>
  
    <div class=" select-none flex items-center justify-center gap-20 h-screen text-xl text-zinc-100">
        <ul class="z-10">
          <li class="cursor-pointer flex flex-col " style="--i:5;--clr:#1877f2"><span class="text-outline">♣</span><h1 class="text-outline">SİNEK</h1>
            <div class="flex flex-row gap-4 overflow-hidden flex-wrap">
      <p class="card text-black bg-white">🂱</p>
      <p class="card text-black bg-white">🂲</p>
      <p class="card text-black bg-white">🂳</p>
      <p class="card text-black bg-white">🂴</p>
      <p class="card text-black bg-white">🂵</p>
      <p class="card text-black bg-white">🂶</p>
      <p class="card text-black bg-white">🂷</p>
      <p class="card text-black bg-white">🂸</p>
      <p class="card text-black bg-white">🂹</p>
      <p class="card text-black bg-white">🂺</p>
      <p class="card text-black bg-white">🂻</p>
      <p class="card text-black bg-white">🂽</p>
      <p class="card text-black bg-white">🂾</p>
    </div>
          </li>
          <li class="cursor-pointer flex flex-col " style="--i:4;--clr:#25d366"><span class="text-outline">♠</span><h1 class="text-outline">MAÇA</h1>
            <div class="flex flex-row gap-4 overflow-hidden flex-wrap">
      <p class="card text-red-600 bg-white">🃁</p>
      <p class="card text-red-600 bg-white">🃂</p>
      <p class="card text-red-600 bg-white">🃃</p>
      <p class="card text-red-600 bg-white">🃄</p>
      <p class="card text-red-600 bg-white">🃅</p>
      <p class="card text-red-600 bg-white">🃆</p>
      <p class="card text-red-600 bg-white">🃇</p>
      <p class="card text-red-600 bg-white">🃈</p>
      <p class="card text-red-600 bg-white">🃉</p>
      <p class="card text-red-600 bg-white">🃊</p>
      <p class="card text-red-600 bg-white">🃋</p>
      <p class="card text-red-600 bg-white">🃍</p>
      <p class="card text-red-600 bg-white">🃎</p>
    </div>
          </li>
          <li class="cursor-pointer flex flex-col " style="--i:3;--clr:#c32aa3"><span class="text-outline">♥</span><h1 class="text-outline">KUPA</h1>
            <div class="flex flex-row gap-4 overflow-hidden flex-wrap">
      <p class="card text-black bg-white">🂡</p>
      <p class="card text-black bg-white">🂢</p>
      <p class="card text-black bg-white">🂣</p>
      <p class="card text-black bg-white">🂤</p>
      <p class="card text-black bg-white">🂥</p>
      <p class="card text-black bg-white">🂦</p>
      <p class="card text-black bg-white">🂧</p>
      <p class="card text-black bg-white">🂨</p>
      <p class="card text-black bg-white">🂩</p>
      <p class="card text-black bg-white">🂪</p>
      <p class="card text-black bg-white">🂫</p>
      <p class="card text-black bg-white">🂭</p>
      <p class="card text-black bg-white">🂮</p>
    </div>
          </li>
          <li class="cursor-pointer flex flex-col " style="--i:2;--clr:#7F65BF"><span class="text-outline">♦</span><h1 class="text-outline">KARO</h1>
            <div class="flex flex-row gap-4 overflow-hidden flex-wrap">
                  <p class="card text-red-600 bg-white">🃑</p>
                  <p class="card text-red-600 bg-white">🃒</p>
                  <p class="card text-red-600 bg-white">🃓</p>
                  <p class="card text-red-600 bg-white">🃔</p>
                  <p class="card text-red-600 bg-white">🃕</p>
                  <p class="card text-red-600 bg-white">🃖</p>
                  <p class="card text-red-600 bg-white">🃗</p>
                  <p class="card text-red-600 bg-white">🃘</p>
                  <p class="card text-red-600 bg-white">🃙</p>
                  <p class="card text-red-600 bg-white">🃚</p>
                  <p class="card text-red-600 bg-white">🃛</p>
                  <p class="card text-red-600 bg-white">🃝</p>
                  <p class="card text-red-600 bg-white">🃞</p>
              </div>
            </li>
          <li class="cursor-pointer flex flex-col " style="--i:1;--clr:#8FBF22"><span class="text-outline" > J</span><h1 class="text-outline">JOKER</h1><div class="flex flex-row gap-4 overflow-hidden">
      <p class="card text-fuchsia-700 bg-white">🂠</p>
      <p class="card text-fuchsia-700 bg-white">🃟</p>
    
    </div></li>
    
      </ul> 
    </div>
  </div>
  <button @click="toggleDark" class="darkModeButton"></button>
    </template>


<script setup>


         import { ref } from "@vue/reactivity"
        const counter = ref(0)
        const toggleDark=()=>{
            counter.value++
            if ( counter.value%2==0)
            document.querySelector("html").setAttribute("class","dark")
            else
            document.querySelector("html").setAttribute("class","")
        } 


</script>
    
    <style scoped>
      ul{
        position: relative;
        transform : skewY(-10deg)
      }
    
      ul li{
        position: relative;
        list-style: none;
        height: 70px;
        width: 120px;
        background: #3e3f46;
        padding: 15px;
        transition: 0.5s;
        z-index: calc(1*var(--i));
      }
      ul li:hover {
        transform: translateX(75px);
        background: var(--clr);
      }
    h1{
        font-size: 20px;
        font-family: Georgia, 'Times New Roman', Times, serif;
      }
      ul li:active > h1{
        font-size: 30px;
        margin: 16px;
        display: flex;
        align-items: center;
        justify-content: center;
      }
      ul li:active > span{
        font-size: 30px;
    
        display: flex;
        align-items: center;
        justify-content: center;
      }
      ul li:active {
    
        width: 500px;
        height: 400px;
        background: var(--clr);
      }
      ul li:last-child:active {
      width: 200px;
    height: 200px;
    background: var(--clr);
    }
      ul li::before{
        content: '';
        position: absolute;
        top: 0;
        left:-40px;
        width: 40px;
        height: 100%;
        background: #3e3f46;
        filter: brightness(0.7);
        transform-origin: right;
        transform: skewY(45deg) ;
        transition: 0.5s;
      }
    
    
      ul li:hover::before{
        background: var(--clr);
        filter: brightness(0.7);
      }
    
      ul li::after{
        content:'';
        position : absolute;
        top:-40px;
        left:0 ;
        width: 100%;
        height: 40px;
        background: #3e3f46;
        filter: brightness(0.9);
        transform-origin: bottom;
        transform: skewX(45deg);
        transition: 0.5s;
      }
      ul li:hover::after{
        background: var(--clr);
        filter: brightness(0.9);
      }
    
    
      ul li:last-child::after{
        box-shadow: -120px 120px 20px rgba(0, 0, 0, 0.25);
      }
      ul li:last-child:active::after{
        box-shadow: -360px 360px 20px rgba(0, 0, 0, 0.25);
      }
    </style>

    