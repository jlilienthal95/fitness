<script lang="ts">
	import '../app.css';

	let { children } = $props();

	const navItemCont = 'flex flex-col items-center justify-between h-[95px]'
	const navIconCont = "h-[70px] flex items-center"
	const navLabelClass = ""
</script>

<div class="relative flex md:flex-row flex-col-reverse w-full h-[100dvh] bg-[#7a612f] ">
	<div class="absolute inset-0 bg-[url(/strange-bullseyes.png)] opacity-50 z-0">

	</div>
	<div id="sidebarCont" class="flex md:flex-col md:h-full md:w-20 w-full justify-around items-center z-10 bg-[#7a612f] md:border-r-[1px] md:border-t-0 border-t-[1px]">
		<div class={navItemCont}>
			<div class={navIconCont}>
				<img src="/navIcons/home.png" alt="home" class="h-[50px]"/>
			</div>
			<label class={navLabelClass} for="home">Home</label>
		</div>
		<div class={navItemCont}>
			<div class={navIconCont}>
				<img src="/navIcons/blog.png" alt="blog" class="h-[70px]"/>
			</div>
			<label  class={navLabelClass} for="blog">Blog</label>
		</div>
		<div class={navItemCont}>
			<div class={navIconCont}>
				<img src="/navIcons/insta.png" alt="instagram" class="h-[62px]"/>
			</div>
			<label  class={navLabelClass} for="insta">Insta</label>
		</div>
		<div class={navItemCont}>
			<div class={navIconCont}>
				<img src="/navIcons/email.png" alt="contact" class="h-[58px]"/>
			</div>
			<label  class={navLabelClass} for="contact">Contact</label>
		</div>

	</div>
	<div class='flex flex-col flex-grow flex-shrink w-full z-1'>
		{@render children()}
	</div>
</div>
