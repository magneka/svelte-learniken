<script>
    import {count} from "../../stores/counter.js";

    function increment() {
        count.update((n) => n + 1);
    }

    function decrement() {
        count.update((n) => n - 1);
    }

    function clear() {
        count.update((n) => 0);
    }
</script>

<button on:click={increment}>Øk med en</button>
<button on:click={decrement}>Minke med en</button>
<button on:click={clear}>Tøm</button>
