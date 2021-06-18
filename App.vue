<template>
    <div>
        <table>
            <tbody>
                <tr>
                    <td></td>
                </tr>
            </tbody>
        </table>

    </div>
</template>

<script>
import axios from 'axios'

export default {
    data(){
        return {
            todos:null
        }
    },
    mounted(){
        console.log('HOLA DESDE MOUNt');
        this.getTodos();
    },
    methods: {
        getTodos(){
            console.log("aqui get")
            axios
            .get('http://127.0.0.1:8000/api/consumir')
            .then(response =>{
                console.log(response)
            })
            .catch(e => console.log(e))
        }
    }
}
</script>

<style>

</style>