<script setup>
// Import necessary components and functions from Vue and other libraries.
import { ref } from 'vue';
import { Link } from '@inertiajs/vue3';
import MapMarkerOutlineIcon from 'vue-material-design-icons/MapMarkerOutline.vue';
import MenuDownIcon from 'vue-material-design-icons/MenuDown.vue';
import MagnifyIcon from 'vue-material-design-icons/Magnify.vue';
import CartMinusIcon from 'vue-material-design-icons/CartMinus.vue';

// Reactive variable to control the visibility of the navigation dropdown.
const showingNavigationDropdown = ref(false);
</script>

<template>
  <!-- Main container for the authenticated layout -->
  <div class="min-w-[1150px] bg-gray-100 h-full">
    <!-- Header section -->
    <div class="flex items-center bg-gray-900 h-[60px] py-2 fixed z-50 min-w-[1150px] w-full">
      <!-- Amazon logo -->
      <div class="flex">
        <Link class="text-white h-[50px] p-2 pt-3 border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
          AMAZON
        </Link>
      </div>

      <!-- Delivery address section -->
      <div class="text-white h-[50px] p-2 border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
        <div class="flex items-center justify-center">
          <MapMarkerOutlineIcon class="pt-2 -ml-1" fillColor="#f5f5f5" />

          <div>
            <div class="text-[13px] text-gray-300 font-extrabold ">
              <div>Delivery to Kenneth</div>
            </div>

            <div class="text-[15px] text-white -mt-1.5 font-extrabold ">
              <div>Johannesburg SW2 SW2</div>
            </div>
          </div>
        </div>
      </div>

      <!-- Search bar section -->
      <div class="flex grow items-center h-[45px] px-1">
        <div class="flex items-center justify-center br-gray-100 border-r border-r-gray-300 font-extrabold text-[11px] text-gray-600 w-[60px] h-[40px] rounded-l-md cursor-pointer ">
          <div class="pt-[3px] ">
            All
          </div>
          <MenuDownIcon fillColor="#5E5E5E" :size="20" class="-mr-2" />
        </div>
        <input class="block w-full border-none border-transparent focus:border-transparent focus:ring-0" type="text" />
        <div class="cursor-pointer bg-orange-300 p-[5px] px-2  rounded-r-md">
          <MagnifyIcon :size="30" />
        </div>
      </div>

      <!-- User account, returns & orders, and cart sections -->
      <div class="flex">
        <!-- Language selection -->
        <div class="h-[50px] p-2 border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
          <div class="flex items-center justify-center mt-2.5 px-1">
            <img src="https://via.placeholder.com/35x20" alt="" />
            <div class="text-[15px] text-white -mt-2 -mr-0.2 font-extrabold">EN</div>
            <MenuDownIcon fillColor="#c2c2c2" :size="20" class="-mr-4 -mt-1.5 pr-1" />
          </div>
        </div>

        <!-- Account & Lists -->
        <div class="h-[50px] p-2 pt-3 border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
          <div class="flex items-center ">
            <div>
              <div class="text-[12px] text-white font-extrabold">
                Hello,
                <span>sign in</span>
              </div>
              <div class="flex items-center">
                <div class="text-[15px] text-white -mt-2 font-extrabold">Account & List</div>
                <MenuDownIcon fillColor="#c2c2c2" :size="20" class="-mr-4 -mt-1.5 pr-1" />
              </div>
            </div>
          </div>
        </div>

        <!-- Returns & Orders -->
        <div class="h-[50px] p-2 pt-3 border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
          <div class="flex items-center ">
            <div>
              <div class="text-[12px] text-white font-extrabold">Returns</div>
              <div class="flex items-center">
                <div class="text-[15px] text-white -mt-2 font-extrabold">& Orders</div>
              </div>
            </div>
          </div>
        </div>

        <!-- Cart -->
        <div class="relative h-[50px] p-2 pt-3 border-[1px] border-gray-900 rounded-sm hover:border-[1px] hover:border-gray-100 cursor-pointer">
          <span class="absolute text-center right-[21px] w-[14px] -top-0 rounded-full text-[20px]">
            <div class="text-orange-400 font-extrabold bg-gray-900 h-[16px]">0</div>
          </span>
          <div class="flex items-center ">
            <CartMinusIcon fillColor="FCFCFC" :size="40" class="-MT-0.5" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


