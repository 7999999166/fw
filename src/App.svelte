<script>
    import {Route} from 'tinro'; 
    import './nedb.min.js';
    import './w3.css';
    import './bootstrap.bundle.min.js';
    import './bootstrap.min.css';
    import Header from './components/Header.svelte';
    import Footer from './components/Footer.svelte';
    import Sample from './pages/Sample.svelte';
    import Inputs from "./pages/Inputs.svelte";
    import Home from './pages/Home.svelte';

    var database1 = new Nedb({filename: 'Product.db', autoload: true });
    var database2 = new Nedb({filename: 'Price.db', autoload: true });
    var database3 = new Nedb({filename: 'Review.db', autoload: true });

</script>

<style>
.aa{
  display: flex;
  background-color: #A4161A;
  height: 100vh;
}


@font-face {
   font-family: "myFont";
   src: url("/ZenAntiqueSoft-Regular.ttf");
   }


</style>
<div class="aa">
<Header></Header>

<Route path="/"><Home></Home></Route>
<Route path="/inputs"><Inputs></Inputs></Route>
<Route path="/sample"><Sample></Sample></Route>

<Footer></Footer>
</div>
