<template>
  <div class="container">
    <h1>vue-popover</h1>
    <p>Below are a few implementations of the component, for more options and events please see the <a href="https://github.com/JFusco/vue-popover/blob/master/README.md#options">README</a> file documentation</p>

    <p>I've added my own custom styles in page to make it look a little more presentable</p>

    <h2>Tests</h2>
    <p>View coverage report <a href="https://jfusco.github.io/vue-popover/coverage/reports/lcov-report/js/index.html">here</a></p>

    <div className="example">
      <h2>Default face and custom content</h2>
      <p>The component provides a default face, which you will most likely want to override - click "popover"</p>



      <pre>&lt;popover name="default"&gt;
    &lt;div slot="content"&gt;
        &lt;ul&gt;
            &lt;li&gt;&lt;a href="https://www.npmjs.com/~jfusco" target="_blank">npmjs.com&lt;/a&gt;&lt;/li&gt;
            &lt;li&gt;&lt;a href="https://github.com/JFusco" target="_blank">github.com&lt;/a&gt;&lt;/li&gt;
        &lt;/ul&gt;
    &lt;/div&gt;
&lt;/popover&gt;</pre>
    </div>

    <div className="example">
      <h2>Custom face for popover</h2>
      <p>Use the "face" slot to inject your own popover face.</p>



      <pre>&lt;popover name="default"&gt;
    &lt;div slot="face"&gt;
        &lt;button>my links&lt;/button&gt;
    &lt;/div&gt;
    &lt;div slot="content"&gt;
        &lt;ul&gt;
            &lt;li&gt;&lt;a href="https://www.npmjs.com/~jfusco" target="_blank">npmjs.com&lt;/a&gt;&lt;/li&gt;
            &lt;li&gt;&lt;a href="https://github.com/JFusco" target="_blank">github.com&lt;/a&gt;&lt;/li&gt;
        &lt;/ul&gt;
    &lt;/div&gt;
&lt;/popover&gt;</pre>
    </div>
  </div>
</template>

<script type="text/babel">
  import popover from '../component/js/Tags.vue'
</script>

<style lang="scss" scoped>
  .default,
  .custom-face {
    .popover {
      &__container {
        ul {
          margin: 0;
          padding: 5px 0;
          list-style: none;
          background: white;
          -webkit-box-shadow: 0 2px 11px -1px rgba(0,0,0,0.51);
          -moz-box-shadow: 0 2px 11px -1px rgba(0,0,0,0.51);
          box-shadow: 0 2px 11px -1px rgba(0,0,0,0.51);
        }

        a {
          display: block;
          text-decoration: none;
          padding: 8px 10px;
          color: black;
          transition: background 0.3s ease;

          &:hover {
            background: lightgray;
          }
        }
      }
    }
  }
</style>
