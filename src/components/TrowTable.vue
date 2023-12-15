<template>
    <tr>
        <td><input @keypress="makeS($event)" :disabled="isEdit ? false : true" type="text" v-model="persItem.name"></td>
        <td>{{ persItem.lname }}</td>
        <td>{{ persItem.birth }}</td>
        <td>
            <div>
                <button @click="isEdit = true">Edit</button>
                <button>Delete</button>
            </div>
        </td>
    </tr>
</template>
<script>
    export default{
        props : ['persItem'],
        data(){
            return {
                isEdit : false
            }
        },
        methods : {
            makeS(e){
                //console.log(e)
                if(e.key == 'Enter'){
                    //console.log('manova donnée')
                    this.$emit('manova-data', this.persItem)
                }
            }
        }
    }
</script>