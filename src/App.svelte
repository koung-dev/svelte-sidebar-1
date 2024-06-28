<script>

  import { clickOutside } from "./lib/clickOutside";
  let showSettings= false
  let showCreate = false
  let showProfile= false

</script>

<div class="bg-no-repeat bg-cover bg-[url('./images/paysage3.jfif')] w-full h-screen flex items-center justify-center">
  <div class="box-border p-4 filter backdrop-blur-xs rounded-lg bg-black/40 text-white w-52">
    <div class="divide-y-2 divide-gray-300 h-full w-full">
      <div class="h-[10%] mb-3 px-2 flex items-center space-x-2">
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-width="2" d="M3 6h18M3 12h18M3 18h18"/></svg>
        <p>Ryan' UI</p>
      </div>
      <div class="">
        <div class="px-2 hover:bg-black/30 hover:rounded-md h-10 flex flex-row items-center mt-2 space-x-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><path d="M21 19v-6.733a4 4 0 0 0-1.245-2.9L13.378 3.31a2 2 0 0 0-2.755 0L4.245 9.367A4 4 0 0 0 3 12.267V19a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2"/><path d="M9 15a2 2 0 0 1 2-2h2a2 2 0 0 1 2 2v6H9z"/></g></svg>
          <p class="">home</p>
        </div>
        <div class="px-2 hover:bg-black/30 hover:rounded-md h-10 flex flex-row items-center space-x-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2 5a2 2 0 0 1 2-2h6v18H4a2 2 0 0 1-2-2zm12-2h6a2 2 0 0 1 2 2v5h-8zm0 11h8v5a2 2 0 0 1-2 2h-6z"/></svg>
          <p>dashboard</p>
        </div>

        <div on:click={()=>{showSettings= true}} use:clickOutside on:click_outside={()=>{showSettings= false}} class="hover:bg-black/30 px-2 hover:rounded-md h-10 flex flex-row items-center justify-between">
          <div class="space-x-2 flex items-center">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-width="2"><path d="M14 3.269C14 2.568 13.432 2 12.731 2H11.27C10.568 2 10 2.568 10 3.269c0 .578-.396 1.074-.935 1.286c-.085.034-.17.07-.253.106c-.531.23-1.162.16-1.572-.249a1.269 1.269 0 0 0-1.794 0L4.412 5.446a1.269 1.269 0 0 0 0 1.794c.41.41.48 1.04.248 1.572a7.946 7.946 0 0 0-.105.253c-.212.539-.708.935-1.286.935C2.568 10 2 10.568 2 11.269v1.462C2 13.432 2.568 14 3.269 14c.578 0 1.074.396 1.286.935c.034.085.07.17.105.253c.231.531.161 1.162-.248 1.572a1.269 1.269 0 0 0 0 1.794l1.034 1.034a1.269 1.269 0 0 0 1.794 0c.41-.41 1.04-.48 1.572-.249c.083.037.168.072.253.106c.539.212.935.708.935 1.286c0 .701.568 1.269 1.269 1.269h1.462c.701 0 1.269-.568 1.269-1.269c0-.578.396-1.074.935-1.287c.085-.033.17-.068.253-.104c.531-.232 1.162-.161 1.571.248a1.269 1.269 0 0 0 1.795 0l1.034-1.034a1.269 1.269 0 0 0 0-1.794c-.41-.41-.48-1.04-.249-1.572c.037-.083.072-.168.106-.253c.212-.539.708-.935 1.286-.935c.701 0 1.269-.568 1.269-1.269V11.27c0-.701-.568-1.269-1.269-1.269c-.578 0-1.074-.396-1.287-.935a7.755 7.755 0 0 0-.105-.253c-.23-.531-.16-1.162.249-1.572a1.269 1.269 0 0 0 0-1.794l-1.034-1.034a1.269 1.269 0 0 0-1.794 0c-.41.41-1.04.48-1.572.249a7.913 7.913 0 0 0-.253-.106C14.396 4.343 14 3.847 14 3.27z"/><path d="M16 12a4 4 0 1 1-8 0a4 4 0 0 1 8 0Z"/></g></svg>
            <p class="">settings</p>
          </div>
          {#if showSettings}
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m6 14l6-6l6 6"/></svg>
          {:else}
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m6 10l6 6l6-6"/></svg>
          {/if}        
        </div>

        <div class:hidden={!showSettings}>
          <div class="px-4 h-10 flex flex-row items-center space-x-3">
            <svg xmlns="http://www.w3.org/2000/svg" width="6" height="6" viewBox="0 0 24 24"><circle cx="12" cy="12" r="11" fill="currentColor"/></svg>
            <p>display</p>
          </div>
          <div class="px-4 h-10 flex flex-row items-center space-x-3">
            <svg xmlns="http://www.w3.org/2000/svg" width="6" height="6" viewBox="0 0 24 24"><circle cx="12" cy="12" r="11" fill="currentColor"/></svg>
            <p>appearance</p>
          </div>
          <div class="px-4 h-10 flex flex-row items-center space-x-3">
            <svg xmlns="http://www.w3.org/2000/svg" width="6" height="6" viewBox="0 0 24 24"><circle cx="12" cy="12" r="11" fill="currentColor"/></svg>
            <p>preferences</p>
          </div>
        </div>

        <div on:click={()=>{showCreate= true}} use:clickOutside on:click_outside={()=>{showCreate= false}} class="hover:bg-black/30 px-2 hover:rounded-md h-10 flex flex-row items-center justify-between">
          <div class="space-x-2 flex items-center">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-width="2" d="M12 20v-8m0 0V4m0 8h8m-8 0H4"/></svg>
            <p class="">create</p>
          </div>
          {#if showCreate}
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m6 14l6-6l6 6"/></svg>
          {:else}
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m6 10l6 6l6-6"/></svg>
          {/if} 
        </div>

        <div class:hidden={!showCreate}>
          <div class="px-4 h-10 flex flex-row items-center space-x-3">
            <svg xmlns="http://www.w3.org/2000/svg" width="6" height="6" viewBox="0 0 24 24"><circle cx="12" cy="12" r="11" fill="currentColor"/></svg>
            <p>articles</p>
          </div>
          <div class="px-4 h-10 flex flex-row items-center space-x-3">
            <svg xmlns="http://www.w3.org/2000/svg" width="6" height="6" viewBox="0 0 24 24"><circle cx="12" cy="12" r="11" fill="currentColor"/></svg>
            <p>document</p>
          </div>
          <div class="px-4 h-10 flex flex-row items-center space-x-3">
            <svg xmlns="http://www.w3.org/2000/svg" width="6" height="6" viewBox="0 0 24 24"><circle cx="12" cy="12" r="11" fill="currentColor"/></svg>
            <p>video</p>
          </div>
          <div class="px-4 h-10 flex flex-row items-center space-x-3">
            <svg xmlns="http://www.w3.org/2000/svg" width="6" height="6" viewBox="0 0 24 24"><circle cx="12" cy="12" r="11" fill="currentColor"/></svg>
            <p>presentation</p>
          </div>
        </div>

        <div on:click={()=>{showProfile= true}} use:clickOutside on:click_outside={()=>{showProfile= false}} class="hover:bg-black/30 px-2 hover:rounded-md h-10 flex flex-row items-center justify-between">
          <div class="space-x-2 flex items-center">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="7" r="5"/><path stroke-linecap="round" stroke-linejoin="round" d="M17 14h.352a3 3 0 0 1 2.976 2.628l.391 3.124A2 2 0 0 1 18.734 22H5.266a2 2 0 0 1-1.985-2.248l.39-3.124A3 3 0 0 1 6.649 14H7"/></g></svg>
            <p class="">profile</p>
          </div>
          {#if showProfile}
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m6 14l6-6l6 6"/></svg>
          {:else}
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m6 10l6 6l6-6"/></svg>
          {/if} 
        </div>
        
        <div class:hidden={!showProfile}>
          <div class="px-4 h-10 flex flex-row items-center space-x-3">
            <svg xmlns="http://www.w3.org/2000/svg" width="6" height="6" viewBox="0 0 24 24"><circle cx="12" cy="12" r="11" fill="currentColor"/></svg>
            <p>avatar</p>
          </div>
          <div class="px-4 h-10 flex flex-row items-center space-x-3">
            <svg xmlns="http://www.w3.org/2000/svg" width="6" height="6" viewBox="0 0 24 24"><circle cx="12" cy="12" r="11" fill="currentColor"/></svg>
            <p>Thème</p>
          </div>
        </div>

        <div class="px-2 hover:bg-black/30 hover:rounded-md h-10 flex flex-row items-center space-x-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><path d="M12.721 5.003L11.255 5c-3.344-.008-6.247 2.709-6.27 6v3.79c0 .79-.1 1.561-.531 2.218l-.287.438C3.73 18.11 4.2 19 4.985 19h14.03c.785 0 1.254-.89.818-1.554l-.287-.438c-.43-.657-.531-1.429-.531-2.219v-3.788c-.04-3.292-2.95-5.99-6.294-5.998M15 19a3 3 0 1 1-6 0"/><path d="M12 2a2 2 0 0 1 2 2v1h-4V4a2 2 0 0 1 2-2"/></g></svg>
          <p>notification</p>
        </div>

        <div class="px-2 hover:bg-black/30 hover:rounded-md h-10 flex flex-row items-center space-x-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-linejoin="round" stroke-width="2"><path d="M5 7h13.79a2 2 0 0 1 1.99 2.199l-.6 6A2 2 0 0 1 18.19 17H8.64a2 2 0 0 1-1.962-1.608z"/><path stroke-linecap="round" d="m5 7l-.81-3.243A1 1 0 0 0 3.22 3H2m6 18h2m6 0h2"/></g></svg>          
          <p>products</p>
        </div>

        <div class="px-2 hover:bg-black/30 hover:rounded-md h-10 flex flex-row items-center space-x-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><rect width="18" height="18" x="3" y="3" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" rx="4"/></svg>
          <p>account</p>
        </div>
      </div>
    </div>
  </div>
</div>