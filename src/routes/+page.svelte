<script lang="ts">
	import Blob from '$lib/components/Blob/Component.svelte';
    import MobileWrapper from "$lib/components/MobileWrapper/Component.svelte"
	const PATHS = [
		'M38.8,-52.7C54.1,-42.2,73.2,-36.1,75.9,-25.3C78.5,-14.5,64.7,1,57.6,17.5C50.6,34,50.3,51.4,41.8,60.1C33.4,68.8,16.7,68.6,-0.3,69C-17.2,69.4,-34.5,70.3,-47.3,63C-60.1,55.8,-68.6,40.4,-68.8,25.7C-69,10.9,-61.1,-3.2,-56.5,-18.6C-51.8,-34.1,-50.5,-50.9,-41.7,-63.6C-32.8,-76.3,-16.4,-84.8,-2.4,-81.5C11.7,-78.3,23.4,-63.3,38.8,-52.7Z',
		'M49.6,-70.4C60.7,-60.2,63.7,-40.9,63.2,-24.8C62.6,-8.6,58.5,4.6,56.5,20.7C54.5,36.9,54.6,56.1,45.6,66.7C36.5,77.3,18.3,79.2,1.1,77.7C-16.1,76.2,-32.2,71.3,-45.6,62.1C-59,53,-69.8,39.6,-72.3,25.1C-74.7,10.7,-68.8,-4.9,-63.3,-20.1C-57.7,-35.3,-52.5,-50.2,-42,-60.7C-31.6,-71.1,-15.8,-77,1.7,-79.4C19.2,-81.8,38.5,-80.6,49.6,-70.4Z',
		'M50.5,-64C65.7,-58.5,78.5,-44.1,79.3,-28.8C80.2,-13.5,69.2,2.7,61.8,18.4C54.4,34.1,50.6,49.3,40.9,58.2C31.2,67.1,15.6,69.7,0,69.7C-15.6,69.7,-31.2,67.1,-40.9,58.1C-50.6,49.2,-54.4,34.1,-60.6,18.8C-66.9,3.5,-75.6,-12,-72,-23.6C-68.5,-35.2,-52.7,-43,-38.7,-48.9C-24.6,-54.7,-12.3,-58.7,2.7,-62.3C17.7,-66,35.3,-69.5,50.5,-64Z',
		'M52.2,-63.2C67.7,-60.6,80.4,-45.4,77.2,-30.8C74,-16.3,55,-2.3,45.7,11.3C36.4,24.9,36.8,38.1,30.8,50.1C24.8,62.1,12.4,72.9,1.1,71.4C-10.2,69.8,-20.4,56,-30.3,45.3C-40.2,34.5,-49.8,26.9,-58,15.6C-66.1,4.3,-72.8,-10.8,-72.3,-27C-71.9,-43.2,-64.3,-60.6,-51,-64C-37.8,-67.3,-18.9,-56.6,-0.3,-56.2C18.3,-55.9,36.7,-65.8,52.2,-63.2Z',
		'M26.4,-45.9C31.6,-32.5,31.4,-21.3,37.7,-10.3C44.1,0.8,56.9,11.7,60.2,25.1C63.4,38.5,57.2,54.3,45.6,66.5C34,78.8,17,87.4,1.2,85.7C-14.5,84,-29,71.9,-41.1,59.8C-53.1,47.7,-62.8,35.6,-67.2,21.9C-71.6,8.2,-70.6,-7.2,-65.3,-20.5C-60,-33.8,-50.4,-44.9,-38.8,-56.2C-27.1,-67.5,-13.6,-79.1,-1.5,-77C10.6,-74.9,21.2,-59.3,26.4,-45.9Z'
	];
</script>

<MobileWrapper>
    <h1>Welcome to your library project</h1>
    <p>Create your package using @sveltejs/package and preview/showcase your work with SvelteKit</p>
    <p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

    <div>
    <Blob duration="5s" ds={PATHS} fill="black"/>
    </div>

    <div class="height"></div>
    <div class="width"></div>
    <div class="height overflow"></div>
</MobileWrapper>

<style>
    div {
        height:200px;
        width:200px;
    }

    .height {
        height:100%;
        width: 50px;
        background:rgba(0,0,255,0.5);

    }
    .width {
        height: 50px;
        width: 100%;
        background: rgba(255,0,0,0.5);
    }

    .height, .width {
        position:absolute;
        top:50%;
        left:50%;
        transform: translate(-50%,-50%);
    }

    .height:before, .width:before{
        content:"start";
    }

    .height:after, .width:after{
        content:"end";
        position:absolute;
        bottom:0;
        right:0;
    }

    .overflow {
        height:200%;
        top:0;
        left:0;
        transform: none;
    }
</style>
