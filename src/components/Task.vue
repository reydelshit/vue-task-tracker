<template>
    <div :class="[task.reminder ? 'reminder' : '', 'task']">
        <h3 >{{task.text}}
            <i @click="onDelete(task.id)" class="fas fa-times"></i>
        </h3>
        <p>{{task.day}}</p>
    </div>

</template>

<script>
export default {
    name: 'Task',
    props: {
        task: Object
    },
    methods: {
        onDelete(id){
            this.$emit('delete-task', id)
        }
    }
}
</script>


<style scoped>

    .reminder{
        border-left: 5px solid green;
    }
    .task{
        font-size: 1rem;
        background: rgb(241, 239, 239);
        margin-bottom: 0.5rem;
        border-radius: 2px;
        padding: 1em;
    }

    h3{
        display: flex;
        justify-content: space-between;
    }

    .fas{
        align-self: center;
        color: red;
        cursor: pointer;
    }
</style>