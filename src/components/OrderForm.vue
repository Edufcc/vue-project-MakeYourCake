<template>
    <div>
        <p>componente de mensagem</p>
        <form id="cake-form">
            <div class="input-container">
                <label for="name">Nome do clinte</label>
                <input type="text" id="name" name="name" v-model="name" placeholder="Digite o seu nome">
            </div>
            <div class="input-container">
                <label for="massa">Escolha o tipo da massa:</label>
                <select name="massa" id="massa" v-model="massa">
                    <option value="">Selecione a massa</option>
                    <option value="chocolate">Chocolate</option>
                </select>
            </div>
            <div class="input-container">
                <label for="recheio">Escolha o recheio:</label>
                <select name="recheio" id="recheio" v-model="recheio">
                    <option value="">Selecione o recheio</option>
                    <option value="chocolate">Chocolate</option>
                </select>
            </div>
            <div id="opcionais-conatiner" class="input-container">
                <label id="opcionais-title" for="opcionais">Selecione os opcionais:</label>
                <div class="checkbox-container">
                    <input type="checkbox" name="opcionai" v-model="opcionais" value="nutella">
                    <span>Nutella</span>
                </div>
            </div>
            <div class="input-container">
                <input type="submit" class="submit-btn" value="Montar meu bolo">
            </div>
        </form>
    </div>
</template>

<script lang="ts">
import { ref } from 'vue';

export default {
    setup() {
        // Dados do formulário (exemplo)
        const cakeType = ref('');

        // Função para lidar com o envio do formulário
        const submitForm = () => {
            // Aqui você pode processar os dados do formulário, por exemplo, enviar uma requisição HTTP para salvar os dados no backend
            console.log('Tipo de bolo:', cakeType.value);
            // Ou fazer algo mais elaborado, como enviar para um servidor
        };

        // Retorna as variáveis e métodos que deseja expor para o template
        return {
            cakeType,
            submitForm
        };
    }
}
</script>

<style scoped>
    #cake-form {
        max-width: 400px;
        margin: 0 auto;
    }

    .input-container {
        display: flex;
        flex-direction: column;
        margin-bottom: 15px;
    }

    label {
        font-weight: bold;
        margin-bottom: 10px;
        color: var(--gray-color);
        padding: 5px 10px;
        border-left: 4px solid #FCBA03;
    }

    input, select {
        padding: 5px 10px;
        width: 300px;
    }

    #opcionais-conatiner {
        flex-direction: row;
        flex-wrap: wrap;
    }

    #opcionais-title{
        width: 100%;
    }

    .checkbox-container {
        display: flex;
        align-items: flex-start;
        width: 50%;
        margin-bottom: 20px;
    }

    .checkbox-container span,
    .checkbox-container input {
        width: auto;
    }

    .checkbox-container span {
        margin-left: 6px;
        font-weight: bold;
    }

    .submit-btn {
        background-color: var(--gray-color);
        color: #FCBA03;
        font-weight: bold;
        border: 2px solid var(--gray-color);
        padding: 10px;
        font-size: 16px;
        margin: 0 auto;
        cursor: pointer;
        transition: .5s;
    }

    .submit-btn:hover {
        background-color: transparent;
        color: var(--gray-color);
    }
    
</style>