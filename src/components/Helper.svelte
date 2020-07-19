<script>
const items = [
  {
    code: '**',
    text: 'to <b>bold</b>',
  },
  {
    code: '*',
    text: 'to <i>italic</i>',
  },
  {
    code: '-',
    text: 'to list',
  }, {
    code: '[text](link)',
    text: 'link',
  }, {
    code: '![alt text](path)',
    text: 'image',
  }
];
</script>

<div class="helper">
  <div class="helper__label">Cheatsheet</div>


	<ul class="helper__list">
    {#each items as item}
      <li class="helper__item">
        <span class="helper__code">{item.code}</span>
        <span class="helper__text">{@html item.text}</span>
      </li>
    {/each}

    <li class="helper__item helper__item--link">
      <a href="https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet" target="_blank">
        Read more about Markdown text styling ⟶
      </a>
    </li>
  </ul>
</div>

<style>
.helper {
  color: #f1f1f1;
  background: #46474E;
  position: fixed;
  bottom: -23%;
  right: 40px;
  padding: 40px;
  justify-content: center;
  box-sizing: border-box;
  border-radius: 5px;
  width: 40%;
  transition: 0.25s ease-in bottom;
}

.helper:hover {
  bottom: 40px;
}

.helper__label {
  text-transform: uppercase;
  font-size: 14px;
  margin-bottom: 10px;
  font-weight: 700;
  letter-spacing: 1px;
  opacity: .2;
}

.helper__item:not(:last-child) {
  margin-bottom: 7px;
}

.helper__item--link {
  color: #ffffff6e;
  margin-top: 20px;
  text-align: center;
  display: block;
}

.helper__item--link > a {
  color: inherit;
  padding: 3px;
  display: inline-block;
}

.helper__text--italic { font-style: italic; }
.helper__text--bold { font-weight: bold; }

.helper__code {
  display: inline-block;
  padding: 5px;
  background: #ffffff1f;
  color: rgba(255, 255, 255, 0.8);
  border-radius: 3px;
  margin-right: 8px;
  min-width: 30px;
  text-align: center;
}
</style>