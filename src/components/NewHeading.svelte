<script>
    import Icon from '@iconify/svelte';
    import { onMount } from 'svelte';
let presence;
let data;
onMount(async () => {
  const { useLanyard } = await import("svelte-lanyard");
  data = useLanyard('892107677608599562');

});

  
  let cordStatus = 'Loading..'
  let badgeColor = ''
   $: artistName = "hello"
   $: songName = "hello"
   $: albumName = "hello"

  let isListening = false
  
$: {
  if($data?.spotify) {
    if($data?.spotify) {
        isListening = true
        artistName = $data?.spotify.artist
        songName =   $data?.spotify.song
        albumName =  $data?.spotify.album
    } else {
        isListening = false
    }
  } else if(!$data?.spotify) {
    console.log("no data")
  }
}

$: {
if($data?.discord_status === 'dnd') {
    cordStatus = "Do not disturb"
    badgeColor = '#ED4245'
  } else if($data?.discord_status === 'idle') {
    cordStatus = "Idle"
    badgeColor = '#FEE75C'
  } else if($data?.discord_status === 'online') {
    cordStatus = "Online"
    badgeColor = '#57F287'
  }  else if($data?.discord_status === 'offline') {
    cordStatus = "Offline"
    badgeColor = 'grey'
  }
}

</script>

<div class="flex px-[30vw] ml-[-3vh] mt-[4vh]">
    <img class="rounded-full w-[16vh] mt-[3vh] ml-[3vh] h-[16vh]" src="https://cdn.discordapp.com/avatars/892107677608599562/436c0d4d651974bf6300a70be5522f96.png?size=1024" alt="">
    <div class="text-[#fff] ml-[3.5vh] mt-[2vh]">
        <p class="text-[#fff] text-[2rem] font-semibold">nate</p>
        <p class="text-[#fff] font-[550]">Software Developer | Computer Scientist</p>
        <div class="flex align-middle items-center mt-[1vh] h-[2vh]"><Icon icon="carbon:dot-mark" width="32" height="32" color={badgeColor} /> <p class="text-[#a8a8a8] font-[550]">{cordStatus}</p></div>
        <div class="flex w-[40vw] align-middle items-center ml-[.4vh] mt-[1vh] h-[2vh]"><Icon icon="mdi:spotify" width="22" height="22" /> <p class="text-[#a8a8a8] font-[550] ml-[.5vh]">
            {isListening ? `Listening to ${songName} by ${artistName} on ${albumName}` : "currently not listening to anything"}
        </p></div>
        <div class="flex flex-row mt-[1.2vh]">
            <!-- <img class="" src="./../lib/github.svg" alt="github">
            <img class="mr-[1vh] ml-[1vh]" src="./../lib/telegram.svg" alt="telegram">
            <img class="mr-[1vh] ml-[1vh]" src="./../lib/keybase.svg" alt="keybase">
            <img class="" src="./../lib/mail.svg" alt="email"> -->
            <a href="https://github.com/r0ckstardev" target="_blank"><Icon class="hover:text-[#8ca4fc] hover:cursor-pointer" icon="mdi:github" color="white"  width="36" height="36" /></a>
            <a href="https://t.me/@rockstarservices" target="_blank"><Icon class="hover:text-[#8ca4fc] mr-[1vh] ml-[1vh] hover:cursor-pointer" icon="mdi:telegram" color="white" width="36" height="36" /></a>
            <a href="https://keybase.io/cxrrupted" target="_blank"><Icon class="hover:text-[#8ca4fc] mr-[1vh] ml-[1vh] hover:cursor-pointer" icon="carbon:logo-keybase" color="white" width="36" height="36" /></a>
            <a href="https://discordapp.com/users/892107677608599562" target="_blank"><Icon class="hover:text-[#8ca4fc] mr-[1vh] ml-[1vh] hover:cursor-pointer" icon="mdi:discord" color="white" width="36" height="36" /></a>
            <!-- <Icon class="hover:text-[#8ca4fc] hover:cursor-pointer" icon="material-symbols:alternate-email" color="white" width="36" height="36" /> -->
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