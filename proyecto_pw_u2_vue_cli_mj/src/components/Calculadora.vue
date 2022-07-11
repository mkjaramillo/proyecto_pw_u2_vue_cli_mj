<template>
  <div>
    <table>
       
        <tr>
           
            <td>
                <h1>Calculadora</h1>
            </td>
            
        </tr>
        
        <tr>
            <td>
              
                <input type="text" v-model="n1"/>
            </td>
            <td>
                
                <input type="text" v-model="n2"/>
            </td>
            <td>
                <p>=</p>
            </td>
            <td>
                <label for="">  {{total}}</label>
            </td>
        </tr>
        <tr>
            <td>
<button  v-on:click="sumar" class="c">+</button>
            </td>
            <td>
<button v-on:click="restar" class="c">-</button>
            </td>
        </tr>
        <tr>
            <td>
<button v-on:click="mult" class="c">x</button>
            </td>
            <td>
 <button v-on:click="div" class="c">/</button>
            </td>
        </tr>
        
    </table>
    
    


    
  </div>
</template>

<script>
export default {
 name: "Calculadora",
  data() {
    return {
      n1: '',
      n2:'',
      total:''
    };
  },
   methods: {
    sumar() {
     return this.total=parseInt(this.n1)+parseInt(this.n2);
      
    },
    restar(){
        return this.total=parseInt(this.n1)-parseInt(this.n2);
    },
    mult(){
        return this.total=parseInt(this.n1)*parseInt(this.n2);
    },
    div(){
        return this.total=parseInt(this.n1)/parseInt(this.n2);
    }
  },
}
</script>

<style>
table{
    margin:auto;
    background: linear-gradient(to bottom, white, rgb(208, 167, 231));

    border: solid 0.1em rgb(51, 5, 51);
}
h1{
    font-family: 'Courier New', Courier, monospace;
    color: rgb(62, 17, 85);
    
}
.c{
    margin: auto;
    background:  rgb(139, 89, 168);
    border: 3em;
    padding: 1.5em;
}
.c:hover{
background: darkorchid;
}
label{
    border: solid 0.1px rgb(102, 94, 94);
    padding-left:0.5em;
    padding-right: 0.5em;
    padding-bottom: 0.1em;
    background: white;
    border-radius: 0.1em;
}

</style>