<script>
  import { Router, Route, link } from "svelte-navigator";
  import Home from "../components/Home.svelte";
  import BirdDetail from "../components/BridDetail.svelte";
  import Favorites from "../components/Favorites.svelte";
  import Navbar from "../components/Navbar.svelte";
</script>

<Router>
  <header class="navbar  is-spaced">
    <Navbar />
  </header>

  <main>
    <Route path="/">
      <Home />
    </Route>
    <Route path="/favorites" component={Favorites} primary={false} />
    <Route path="/:uid" component={BirdDetail} primary={false} />
  </main>
</Router>
