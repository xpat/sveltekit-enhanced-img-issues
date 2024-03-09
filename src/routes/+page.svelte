<script lang="ts">
    import myPNG from '../images/pinkmonsterteethy.png?enhanced';
    const fileName = "pinkmonsterteethy";
    const fileExtension = "png";
    const pathToFileTemplate = `../images/${fileName}.${fileExtension}`;
    const pathToFile = '../images/pinkmonsterteethy';
</script>

<div>
     <!-- these work fine -->
     <enhanced:img src={myPNG} alt='' />
     <enhanced:img src='../images/pinkmonsterteethy.png' alt="" />
</div>

<!--- Without Typescript, const and div -->
<script>
     import myPNG from '../images/pinkmonsterteethy.png?enhanced';
     import myVideo from '../images/video1.mp4?enhanced';
     import myGIF from '../images/image.gif?enhanced';
</script>


     <!-- these work fine -->
     <enhanced:img src={myPNG} alt='' />
     <enhanced:img src='../images/pinkmonsterteethy.png' alt="" />

     <!-- these partially work -GIFs appear using either the variable or the path -->
     <enhanced:img src={myGIF} alt='' />
     <enhanced:img src='../images/image.gif' alt="" />
         
     <!-- these don't work -->
     <enhanced:img src={myVideo} alt='' />
     <enhanced:img src='../images/video1.mp4' alt="" />


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
