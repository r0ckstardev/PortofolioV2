<script>
    import Icon from '@iconify/svelte';
</script>

<div class="flex px-[30vw] mt-[4vh]">
    <img class="rounded-full w-[16vh] h-[16vh]" src="https://cdn.discordapp.com/avatars/892107677608599562/436c0d4d651974bf6300a70be5522f96.png?size=1024" alt="">
    <div class="text-[#fff] ml-[3.5vh] mt-[2vh]">
        <p class="text-[#fff] text-[2rem] font-semibold">nate</p>
        <p class="text-[#fff] font-[550]">Software Developer | Computer Scientist</p>
        <div class="flex align-middle items-center mt-[1vh] h-[2vh]"><Icon icon="carbon:dot-mark" width="32" height="32" /> <p class="text-[#a8a8a8] font-[550]">Offline</p></div>
        <div class="flex align-middle items-center ml-[.4vh] mt-[1vh] h-[2vh]"><Icon icon="mdi:spotify" width="22" height="22" /> <p class="text-[#a8a8a8] font-[550] ml-[.5vh]">Currently Not Listening to anything</p></div>
        <div class="flex flex-row mt-[1.2vh]">
            <!-- <img class="" src="./../lib/github.svg" alt="github">
            <img class="mr-[1vh] ml-[1vh]" src="./../lib/telegram.svg" alt="telegram">
            <img class="mr-[1vh] ml-[1vh]" src="./../lib/keybase.svg" alt="keybase">
            <img class="" src="./../lib/mail.svg" alt="email"> -->
            <Icon class="hover:text-[#8ca4fc] hover:cursor-pointer" icon="mdi:github" color="white"  width="36" height="36" />
            <Icon class="hover:text-[#8ca4fc] mr-[1vh] ml-[1vh] hover:cursor-pointer" icon="mdi:telegram" color="white" width="36" height="36" />
            <Icon class="hover:text-[#8ca4fc] mr-[1vh] ml-[1vh] hover:cursor-pointer" icon="carbon:logo-keybase" color="white" width="36" height="36" />
            <Icon class="hover:text-[#8ca4fc] mr-[1vh] ml-[1vh] hover:cursor-pointer" icon="mdi:discord" color="white" width="36" height="36" />
            <Icon class="hover:text-[#8ca4fc] hover:cursor-pointer" icon="material-symbols:alternate-email" color="white" width="36" height="36" />
        </div> 
    </div>
</div>
<div class="flex px-[30vw] mt-[1.2vh]">
    <p class="text-[#a8a8a8] pl-[2vh] mt-[1.5vh] text-lg font-semibold">
        Hello! I'm nate, I'm a 17 year old <span class="text-[#8ca4fc]">programmer</span> and a <span class="text-[#8ca4fc]">computer</span> scientist from Turkey
        I've started my programming journey with <span class="text-[#f7df1e]">Javascript</span> currently I'm learning <span class="text-[#00ADD8]">Golang</span> & <span class="text-[#A55D35]">Rust</span> I enjoy reading Books, Watching Shows & Anime, Listening to music and programming.
        to learn more you can head to my <a href="" class="text-[#8ca4fc] hover:cursor-pointer hover:underline ">blog (soon) &rarr</a>
    </p>
</div>