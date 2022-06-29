<template>
<div class="shadow rounded-md p-4 ml-2 mb-2 bg-white align-left" :class="{'shadow rounded-md p-2 bg-gradient-to-r from-cyan-500 to-blue-500' : isActive}">
    <div class="flex flex-col">
        <div class="">
            <h3 class="font-bold leading-tight text-1xl mt-0 mb-2 text-blue-800">
                {{title}}
            </h3>
        </div>

        <div class="flex items-baseline mb-2">
            <div class="flex-initial w-30 mr-3">
                <span class="font-bold text-sm text-blue-900">
                    &#163; {{priceOne}}
                </span>
            </div>
            <div class="flex-initial w-30">
                <h2 class="font-bold text-sm">+&#163; {{priceMin}}</h2>
            </div>
        </div>

        <div class="flex items-baseline">
            <div class="flex-none w-14">
                <span class="material-icons"> {{icon}}</span>
            </div>
            <div class="flex-initial w-30 text-gray-400 mr-3 text-sm">
                Last Week:
            </div>
            <div class="flex-initial w-30">
                <h2 class="font-bold text-sm flex-b">&#163; {{priceTwo}}</h2>
            </div>
        </div>
    </div>
</div>
</template>
<script>
export default {
    props: {
        title: String,
        priceMin: Number,
        priceOne: Number,
        priceTwo: Number,
        icoColor: String,
        icon: String,
        gradientBg: String,           
    },
    data(){return{
        isActive: false,

    }}
    
}
</script>
<style lang="scss" scoped>
.grid {
  @media (min-width: 768px) {
    flex-direction: column;
  }

  &h3 {
    color: #174c6f;
  }
}

.material-icons {
  background: #c5d5cb;
  color: #51b176;
  padding: 4px;
  border-radius: 4px;
}
</style>