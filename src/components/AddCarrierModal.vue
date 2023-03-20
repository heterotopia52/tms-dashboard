<template>
    <section>
      <button class="bg-orange-500 text-grey active:bg-orange-600 font-bold uppercase text-sm px-6 py-3 rounded shadow hover:shadow-lg outline-none focus: ring focus: ring-orange-300 mr-1 mb-1 leading-snug hover:text-white hover:opacity-85 ease-linear transition-all duration-350" type="button" v-on:click="toggleModal()">
        Add new Carrier
      </button>
      <div v-if="showModal" class="overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
        <div class="relative w-auto my-6 mx-auto max-w-3xl">
          <!--content-->
          <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
            <!--header-->
            <div class="flex items-start justify-between p-5 border-b border-solid border-slate-200 rounded-t">
              <h3 class="text-3xl font-semibold">
                Add new Carrier
              </h3>
              <button class="p-1 ml-auto bg-transparent border-0 text-black opacity-5 float-right text-3xl leading-none font-semibold outline-none focus:outline-none" onclick="carriersModal('modal-carrier')">
                 <span class="bg-transparent text-black opacity-5 h-6 w-6 text-2xl block outline-none focus:outline-none">
                   ×
                 </span>
              </button>
            </div>
            <!--body-->
            <div class="relative p-4 flex-auto">
                <span class="z-10 h-full leading-relaxed font-normal absolute text-center text-slate-300 absolute bg-transparent rounded text-base items-center justify-center w-8 pl-3 py-3">
                   <i class="fas fa-dolly-flatbed text-blueGray-400 mr-2 text-sm"></i> 
                </span>
                <input type="text" placeholder="CarrierID" class="px-2 py-3 placeholder-slate-300 text-slate-600 relative bg-white bg-white rounded text-sm border-0 shadow outline-none focus:outline-none focus:ring w-full pl-10"/>
            </div>
            <div class="relative p-4 flex-auto">
                <span class="z-10 h-full leading-relaxed font-normal absolute text-center text-slate-300 absolute bg-transparent rounded text-base items-center justify-center w-8 pl-3 py-3">
                   <i class="far fa-address-card"></i>
                </span>
                <input type="text" placeholder="Name" class="px-2 py-3 placeholder-slate-300 text-slate-600 relative bg-white bg-white rounded text-sm border-0 shadow outline-none focus:outline-none focus:ring w-full pl-10"/>
            </div>
            <div class="relative p-4 flex-auto">
                <span class="z-10 h-full leading-relaxed font-normal absolute text-center text-slate-300 absolute bg-transparent rounded text-base items-center justify-center w-8 pl-3 py-3">
                  <i class="fas fa-star"></i>
                </span>
                <input type="text" placeholder="Rate" class="px-2 py-3 placeholder-slate-300 text-slate-600 relative bg-white bg-white rounded text-sm border-0 shadow outline-none focus:outline-none focus:ring w-full pl-10"/>
            </div>
            <div class="relative p-4 flex-auto">
                <span class="z-10 h-full leading-relaxed font-normal absolute text-center text-slate-300 absolute bg-transparent rounded text-base items-center justify-center w-8 pl-3 py-3">
                  <i class="fas fa-percentage"></i>
                </span>
                <input type="text" placeholder="Discount" class="px-2 py-3 placeholder-slate-300 text-slate-600 relative bg-white bg-white rounded text-sm border-0 shadow outline-none focus:outline-none focus:ring w-full pl-10"/>
            </div>
            <div class="relative p-4 flex-auto">
                 <span class="z-10 h-full leading-relaxed font-normal absolute text-center text-slate-300 absolute bg-transparent rounded text-base items-center justify-center w-8 pl-3 py-3">
                   <i class="fas fa-bullseye"></i>
                 </span>
                <input type="text" placeholder="Performance" class="px-2 py-3 placeholder-slate-300 text-slate-600 relative bg-white bg-white rounded text-sm border-0 shadow outline-none focus:outline-none focus:ring w-full pl-10"/>
            </div>
            <!--footer-->
            <div class="flex items-center justify-end p-6 border-t border-solid border-slate-200 rounded-b">
                <button class="text-red-500 bg-transparent border border-solid border-red-500 hover:bg-red-500 hover:text-white active:bg-red-600 font-bold uppercase text-sm px-6 py-3 rounded outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button" v-on:click="toggleModal()">
                   Close
                 </button>
                <button class="bg-emerald-500 text-white active:bg-emerald-600 font-bold uppercase text-sm px-6 py-3 rounded shadow hover:shadow-lg outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button" v-on:click="toggleModal()">
                   Save Changes
                </button>
            </div>
          </div>
        </div>
      </div>
      <div v-if="showModal" class="opacity-25 fixed inset-0 z-40 bg-black"></div>
    </section>
  </template>
  
  <script>
  export default {
    name: "add-carrier-modal",
    data() {
      return {
        showModal: false
      }
    },
    methods: {
      toggleModal: function(){
        this.showModal = !this.showModal;
      }
    }
  }
  </script>