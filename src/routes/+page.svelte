<script lang="ts">
    import svelteLogo from '../images/svelte-logo-square.png?enhanced';
    const fileName = "svelte-logo-square";
    const fileExtension = "png";
    const pathToFileTemplate = `../images/${fileName}.${fileExtension}`;
    const pathToFile = '../images/svelte-logo-square.png';
</script>

<div>
    <!-- these work fine -->
    <enhanced:img src={svelteLogo} alt="" />
    <enhanced:img src='../images/svelte-logo-square.png' alt="" />
    
    <!-- these don't work -->
    <enhanced:img src={'../images/svelte-logo-square.png'} alt="" />
    <enhanced:img src={`../images/${fileName}.${fileExtension}`} alt="" />
    <enhanced:img src={pathToFileTemplate} alt="" />
    <enhanced:img src={pathToFile} alt="" />
</div>