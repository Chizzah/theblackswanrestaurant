<template>
  <section>
    <h2>Appetisers</h2>
    <section >
      <section>
        <h3>{{ page.appetisers.name }}</h3>
        <h4>{{ page.appetisers.description }}</h4>
      </section>
      <section>
        <h5>{{ page.appetisers.price }}</h5>
      </section>
    </section>
  </section>
</template>

<page-query>
query Appetisers($path: String!) {
  appetisers: contentfulAppetisers(path: $path) {
    id
    name
    description
    price
  }
}
</page-query>