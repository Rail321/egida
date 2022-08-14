<template>
  <div>
    <div class="row min-h-100vh page">
      <div class="col-12 col-lg-2">
        <div class="navigation h-100vh top-0 position-sticky overflow-lg-auto" ref="navigation">
          <div v-for="index of 15" v-bind:key="index">
            <a href="/">Link</a>
          </div><br>
        </div>
      </div>
      
      <div class="col-12 col-lg-10">
        <h1>Page</h1><br><br>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tenetur nostrum, sunt quisquam amet maxime atque reprehenderit doloremque blanditiis accusamus ut totam nulla, laudantium repellendus officiis quo cumque beatae! Neque, magnam!</p><br>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sint, cupiditate ab, autem porro placeat molestiae minima cum maxime ex esse laboriosam ea doloribus reprehenderit atque labore! Dolores neque alias officia?
        Error doloremque ad voluptatem tempore perspiciatis repellat, eos nihil commodi odit? Pariatur maxime aliquam deserunt repudiandae sit ex nobis veritatis accusamus dignissimos rerum distinctio placeat, laboriosam fugiat quas corporis cumque?</p><br><br>

        <h2>Heading</h2><br>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Doloribus velit aspernatur rem itaque est ipsum aut impedit, rerum ratione natus ipsa tempora? Doloremque maxime temporibus aspernatur quaerat necessitatibus ea fugit.
        Et quibusdam laudantium quasi deserunt, assumenda voluptatum in dolorum soluta eum. Iure ad non, odio obcaecati dolorum doloremque corrupti recusandae corporis exercitationem nam est labore inventore, similique unde aperiam quae?
        Ullam nobis fugit error at eos quam soluta non eius libero nostrum expedita esse, recusandae numquam deserunt necessitatibus! Tempore beatae esse, tenetur reprehenderit itaque saepe ipsum aperiam voluptatibus voluptatum alias!</p><br>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Veritatis sapiente dicta voluptatibus ducimus autem tenetur reprehenderit laudantium illo accusamus itaque placeat quibusdam accusantium voluptatem, labore corporis pariatur sequi earum sunt.
        Fuga distinctio in esse quos necessitatibus minima facere error eos natus, quo repudiandae veritatis ut consequatur. Dolores, fugit aliquid, eveniet ratione quaerat excepturi odio ullam, nobis voluptates expedita natus ipsam.</p>
      </div>
    </div>
  </div>
</template>

<script setup>
  const navigation = ref( null )

  const onScroll = () => navigation.value.scrollTop = navigation.value.scrollHeight * ( window.scrollY / document.body.scrollHeight )

  onMounted( () => {
    onScroll()
    window.addEventListener( 'scroll', onScroll )
  } )
</script>


<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .row {
    display: flex;
    flex-wrap: wrap;
  }

  .col-3, .col-9 {
    min-width: 0;
  }

  .col {
    flex-grow: 1;
    width: auto;
  }

  .col-12 {
    width: 100%;
  }

  @media ( min-width: 992px ) {
    
    .col-lg-2 {
      width: 16.666666%;
    }
    
    .col-lg-10 {
      width: 83.333333%;
    }

    .overflow-lg-auto {
      overflow-y: auto;
    }
    
  }

  .min-h-100vh {
    min-height: 100vh;
  }

  .h-100vh {
    height: 100vh;
  }

  .top-0 {
    top: 0;
  }

  .position-sticky {
    position: sticky;
  }

  body {
    overflow-y: overlay;
    padding-right: 15px;
    background-color: lavender;
  }
  body::-webkit-scrollbar {
    width: 15px;
  }
  body::-webkit-scrollbar-track {
    background-color: transparent;
  }
  body::-webkit-scrollbar-thumb {
    border-radius: 7.5px;
    border: 4px solid lavender;
    background-color: rgba(25, 25, 112, .5);
  }

  .navigation {
    overflow-y: overlay;
    padding-right: 15px;
    background-color: midnightblue;
  }
  .navigation::-webkit-scrollbar {
    width: 15px;
  }
  .navigation::-webkit-scrollbar-track {
    background-color: transparent;
  }
  .navigation::-webkit-scrollbar-thumb {
    border-radius: 7.5px;
    border: 4px solid midnightblue;
    background-color: rgb(230, 230, 250, .5)
  }
</style>