<template>
    <div>
        <table>
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Last name</th>
                    <th>Birth date</th>
                    <th>Actions</th>
                </tr>
            </thead>
            <tbody>
                <TrowTable @manova-data="ovayLeData" v-for="p in pers" :key="p.id" :persItem = "p" />
            </tbody>
        </table>
    </div>
</template>
<script>
import TrowTable from './components/TrowTable.vue';
export default {
    data() {
        return {
            pers : [
                {
                    id : 1,
                    name : "Rakoto",
                    lname : "Jean Baptiste",
                    birth : "2000-05-01"
                },
                {
                    id : 2,
                    name : "Rakoto dddd",
                    lname : "Jean Baptiste",
                    birth : "2000-05-01"
                },
                {
                    id : 3,
                    name : "Rakoto dddd hhhh",
                    lname : "Jean Baptiste",
                    birth : "2000-05-01"
                }
            ]
        }
    },
    components:{TrowTable},
    methods: {
        ovayLeData(data){
            console.log(data)
        }
    }
}
</script>