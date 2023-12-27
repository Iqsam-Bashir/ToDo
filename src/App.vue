<script setup>
import imgUrl from './assets/images/main.jpg'
</script>
<template>
<div class="container">
    <div class="card">
        <img :src="imgUrl">
        <section>
            <header>
                <h1 class="heading">Todos</h1>
                <input class="new-todo" autofocus placeholder="What needs to be done?">
            </header>
            <section class="main">
                <label for="toggle-all">Mark all as complete</label>
                <ul class="todo-list">
                    <li class="todo">
                        <div class="view">
                            <input class="toggle" type="checkbox">
                            <label></label>
                            <button class="destroy"></button>
                        </div>

                    </li>
                </ul>
            </section>
            <footer class="footer">
                <span class="todo-count">
                    <strong></strong>
                    <span> left</span>
                </span>
                <ul class="filters">
                    <li>
                        <a href="#/all">All</a>
                    </li>
                    <li>
                        <a href="#/active">Active</a>
                    </li>
                    <li>
                        <a href="#/completed">Completed</a>
                    </li>
                </ul>
                <button class="clear-completed">
                    Clear completed
                </button>
            </footer>
        </section>
    </div>

</div>
</template>

<style scoped>
@import "https://unpkg.com/todomvc-app-css@2.4.1/index.css";

*,
*:before,
*:after {
    box-sizing: inherit;
    font-family: 'Courier New', Courier, monospace;
}

.container {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: auto;
    padding: 30px;
    font: 1em/1.618 Inter, sans-serif;
}

.card {
    padding: 35px;
    border: 1px solid rgba(255, 255, 255, .25);
    border-radius: 20px;
    background-color: rgba(255, 255, 255, 0.45);
    box-shadow: 0 0 10px 1px rgba(0, 0, 0, 0.25);
    backdrop-filter: blur(15px);
}
.heading{
  color:#cca3ff
}
.todo-count{
   color: red;
}
.filters> li:nth-child(2) > a{
  color:green;
}
</style>
