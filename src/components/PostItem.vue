<template>
    <div class="post">
        <div>
            <h3 class="post__title"><strong>Название:</strong> {{ post.title }} id: {{post.id}}</h3>
            <div class="post__body">{{ post.body }}</div>
        </div>
        <div class="post__buttons">
            <my-button class="post__button-delete"
                @click="$emit('delete', post)"
            >
                Удалить
            </my-button>
        </div>
    </div>
</template>
<script>

export default {
    props: {
        post: {
            type: Object,
            required: true,
        }
    },
    methods: {
    },
}
</script>
<style scoped>
.post {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: #141615;
    padding: 10px;
    border-radius: 10px;
}

.post__title {
    margin-bottom: 10px;
}

.post__body {
    flex-grow: 1;
    border-radius: 5px;
    border: 1px solid grey;
    padding: 10px;
}
.post__button-delete{
    align-self: end;
    margin-top: 5px;
}
</style>