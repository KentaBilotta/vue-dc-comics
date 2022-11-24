<template>
  <header>
    <div><img src="@/img/dc-logo.png" alt="dc-logo"></div>
    <div>
      <ul>
        <li>characters</li>
        <li>comics</li>
        <li>movies</li>
        <li>tv</li>
        <li>games</li>
        <li>collectibles</li>
        <li>videos</li>
        <li>fans</li>
        <li>news</li>
        <li>shop</li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderPage',
};
</script>

<style lang="scss" scoped>

$main-blue: #0282f9;

header{
  display: flex;
  align-items: center;
  justify-content: space-around;
  padding: .5rem;
}

ul{
  display: flex;
  list-style: none;
  text-transform: uppercase;

  li{
    padding: 1rem;
    border-bottom: 5px solid white;
    cursor: pointer;

    &:hover{
      color: $main-blue;
      border-bottom: 5px solid $main-blue;
    }

  }

}

</style>
