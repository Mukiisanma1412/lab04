<template>
    <div> 
        <h1> {{ event.tittle}} </h1>
        <p> {{ event.time }} on {{ event.date }} @ {{ event.location }} </p>
        <p> {{ event.description }} </p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                event: null,
                id: 123
            }
        },
        created() {
        //fetch event(by id) and local event data
        EventService.getEvents(this.id)
            .then(response => {
                this.event = response.data
            })
            .catch(error => {
                console.log(error)
            })
        }
    }
</script>