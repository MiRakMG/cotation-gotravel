<template>
 <form action="">
    <label>Numéro </label><input type="number" required v-model="num">
    <label>Jour </label><input type="date" required v-model="jour">
    <label>Nombres de voyageurs </label><input type="number" required v-model="nbrVoyageur">
    <label>Préstations </label><input type="number" required v-model="prestation" placeholder="€">
    <label>Charges </label><input type="number" required v-model="charges" placeholder="Ar">
    <button class="btn-vert">Valider</button><button class="btn" type="reset">Annuler</button>
 </form>
 <table class="content-table">
    <thead>
    <tr>
        <th>Coût Unitaire</th>
        <th>Charges</th>
        <th>Nombres de voyageurs</th>
        <th>Total</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>{{ prestation*4100 }}</td>
        <td>{{ charges || 0 }}</td>
        <td>{{ nbrVoyageur || 0 }}</td>
        <td>{{ (prestation*4100)+(charges*nbrVoyageur) || 0 }}</td>
    </tr>
    <tr>
        <td>{{  }}</td>
        <td>{{  }}</td>
        <td>{{  }}</td>
        <td>{{  }}</td>
    </tr>
    <tr>
        <td>{{  }}</td>
        <td>{{  }}</td>
        <td>{{  }}</td>
        <td>{{  }}</td>
    </tr>
    <tr>
        <td>{{  }}</td>
        <td>{{  }}</td>
        <td>{{  }}</td>
        <td>{{  }}</td>
    </tr>
    </tbody>
 </table>
</template>

<script>
    export default {
        data() {
            return {
                num: '',
                jour: '',
                nbrVoyageur: '',
                prestation: '',
                charges: ''
            }
        }
    }
</script>

<style>
    button {
        padding: 10px;
        margin: 2px ;
        border-radius: 5px;
        letter-spacing: 1px;
    }
    .btn-vert {
        color: white;      
        background-color: rgb(76, 167, 40);
        border: none;
    }
    .btn {
        color: white;
        background-color: red;
        border: none;
    }
    form {
        max-width: 420px;
        margin: 30px auto;
        background-color: white;
        text-align: left;
        padding: 30px;
        border-radius: 10px;
    }
    label {
        color: #aaa;
        display: inline-block;
        margin: 25px 0 15px;
        font-size: 0.6em;
        text-transform: uppercase;
        letter-spacing: 1px;
        font-weight: bold;
    }
    input {
        display: block;
        padding: 10px 6px;
        width: 100%;
        box-sizing: border-box;
        border: none;
        border-bottom: 1px solid #ddd;
        color: #555;
    }
    .content-table {
        border-collapse: collapse;
        background-color: white;
        margin:25px 0;
        font-size: 0.5cm;
        min-width: 800px;
        border-radius: 15px ;
        overflow: hidden;
    }

    .content-table thead tr {
        background-color: rgb(44, 70, 155);
        color: white;
        text-align: center;
        font-weight: bold;
    }
    
    .content-table th,
    .content-table td {
        padding: 12px 16px;
    }

    .content-table tbody tr {
        border-bottom: 1px solid #dddddd;
    }

    .content-table tbody tr:nth-of-type(even) {
        background-color: #f3f3f3;
    }

    .content-table tbody tr:last-of-type {
        border-bottom: 2px solid rgb(6, 32, 117);
    }

</style>