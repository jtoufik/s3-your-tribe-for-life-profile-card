<script>
  /** @type {import("@prismicio/client").Content.HomeSlice} */
  export let slice;
  console.log(slice)
</script>

<section data-slice-type={slice.slice_type} data-slice-variation={slice.variation}>

  <svg preserveAspectRatio="xMidYMid slice" viewBox="10 10 80 80">
    <defs></defs>
    <path fill="#4f4e4f" class="out-top" d="M37-5C25.1-14.7,5.7-19.1-9.2-10-28.5,1.8-32.7,31.1-19.8,49c15.5,21.5,52.6,22,67.2,2.3C59.4,35,53.7,8.5,37-5Z"/>
    <path fill="#97b392" class="in-top" d="M20.6,4.1C11.6,1.5-1.9,2.5-8,11.2-16.3,23.1-8.2,45.6,7.4,50S42.1,38.9,41,24.5C40.2,14.1,29.4,6.6,20.6,4.1Z"/>
    <path fill="#ffdf5e" class="out-bottom" d="M105.9,48.6c-12.4-8.2-29.3-4.8-39.4.8-23.4,12.8-37.7,51.9-19.1,74.1s63.9,15.3,76-5.6c7.6-13.3,1.8-31.1-2.3-43.8C117.6,63.3,114.7,54.3,105.9,48.6Z"/>
    <path fill="#757460" class="in-bottom" d="M102,67.1c-9.6-6.1-22-3.1-29.5,2-15.4,10.7-19.6,37.5-7.6,47.8s35.9,3.9,44.5-12.5C115.5,92.6,113.9,74.6,102,67.1Z"/>
  </svg>

  <section class="card">
    <img src= {slice.primary.profileimg.url} alt="Profiel foto">

    <h1>{slice.primary.title}</h1>

    <p>{slice.primary.paragraaf[0].text}</p> 
  </section>


</section>


<style>

@font-face {
  font-family: 'NeonClubMusic';
  src: url('/src/lib/slices/Home/fonts/NEON-CM/NEON\ CLUB\ MUSIC_bold.otf');
}

  section{
    display: grid;
    place-items: center;
    height: 100vh;

    font-family: roboto, helvetica, arial, sans-serif;
  }

  .card{
    z-index: 1;

    background-color: rgba(255, 255, 255, 0.768);
    backdrop-filter: blur(5px);  
    box-shadow: 0px 15px 59px -35px rgba(161,161,161,1);

    width: 24em;
    height: 32em;

    border: 3px solid rgba(211, 211, 211, 0.762);
    border-radius: 5px;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  img {
    max-width: 155px; 
    height: auto; 
    display: block; 
    margin: 0 auto; 
    border-radius: 50%;
    border: 3px solid rgb(178, 178, 178);
  }

  h1{
    font-family: NeonClubMusic;
    padding-top: 1em;
  }

  p{
    max-width: 18em;
    text-align: center;
    border-top: solid 3px grey;
    padding-top: 2em;
    letter-spacing: 2px;
  }

  /* background animatie */


  @keyframes rotate {
      0% {
          transform: rotate(0deg);
      }
      100% {
          transform: rotate(360deg);
      }
  }
  .out-top {
      animation: rotate 20s linear infinite;
      transform-origin: 13px 25px;
  }
  .in-top {
      animation: rotate 10s linear infinite;
      transform-origin: 13px 25px;
  }
  .out-bottom {
      animation: rotate 25s linear infinite;
      transform-origin: 84px 93px;
  }
  .in-bottom {
      animation: rotate 15s linear infinite;
      transform-origin: 84px 93px;
  }

  svg {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
  }

</style>