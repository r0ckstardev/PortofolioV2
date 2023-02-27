<script>
	import { useLanyard } from "sk-lanyard";
        const presence = useLanyard({ method: 'ws', id: '892107677608599562' });
</script>
<code class="text-[#fff]">{JSON.stringify($presence ?? {}, null, 2)}</code>