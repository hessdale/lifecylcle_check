<template>
    <div>

    </div>
</template>

<script>
    export default {
        data() {
            return {
                tweets:[`tweet1`,`tweet2`,`tweet3`],
                num_friends:1,
                logged_in:false,
            }
        },
        methods: {
            show_info:function(){
            document.querySelector(`div`).insertAdjacentHTML(`beforeend`,`<p>friends: ${this.num_friends}</p><p>logged in:${this.logged_in}</p>`)
            for (let index = 0; index < this.tweets.length; index++) {
            document.querySelector(`div`).insertAdjacentHTML(`beforeend`,`<h3>${this.tweets[index]}</h3>`);
}
        },
        mounted (){
            this.show_info
            }
        },
    };
</script>

<style scoped>

</style>