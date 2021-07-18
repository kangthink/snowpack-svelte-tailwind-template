<script>
  import './main.css'
  import {onMount} from 'svelte';
  import Hello from './components/Hello.svelte'

  let count = 0;
  onMount(() => {
    const interval = setInterval(() => count++, 1000);
    return () => {
      clearInterval(interval);
    };
  });
</script>

<div class="app">
  <div class="px-5 bg-green-300 box">
    <div>TS Timer {count}</div>
  </div>
</div>
