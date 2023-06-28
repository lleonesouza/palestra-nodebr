<template>
    <div class="api-calls">
        <ul>
            <li class="api-header">
                <div>Método</div>
                <div>Rota</div>
                <div class="action">Ação</div>
            </li>
            <li class="api-call" v-for="call in apiCalls" :key="call.id" v-click="highlightRoute(call.id)"
                :class="{ 'highlighted': highlightedRoute === call.id }">
                <div class="method">{{ call.method }}</div>
                <div class="endpoint">{{ call.endpoint }}</div>
                <div class="description">{{ call.description }}</div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            apiCalls: [
                { id: 1, method: 'POST', endpoint: '/health', description: 'Está vivo?' },
                { id: 2, method: 'POST', endpoint: '/read', description: 'Pede temperatura e humidade' },
                { id: 3, method: 'POST', endpoint: '/run', description: 'Roda motor para frente' },
                { id: 4, method: 'POST', endpoint: '/back', description: 'Roda motores para trás' },
                { id: 5, method: 'POST', endpoint: '/turn-left', description: 'Vira para esquerda' },
                { id: 6, method: 'POST', endpoint: '/turn-right', description: 'Vira para direita' },
                { id: 7, method: 'POST', endpoint: '/stop', description: 'Para os motores' }
            ],
            highlightedRoute: null
        };
    },
    methods: {
        highlightRoute(id) {
            this.highlightedRoute = id;
        }
    }
};
</script>

<style scoped>
.api-calls {
    font-family: Arial, sans-serif;
}

.api-call {
    padding: 5px;
    margin: auto;
    border-radius: 5px;
    display: flex;
    background: rgba(255, 255, 255, 0.05);
    gap: 50px;
}

.api-header {
    padding: 5px;
    margin: auto;
    border-radius: 5px;
    display: flex;
    background: rgba(255, 255, 255, 0.11);
    gap: 100px;
}


.api-header div {
    padding: 5px;
    margin-left: 10px;
    margin-right: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
}



.method {
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    letter-spacing: 0.5px;
    color: green;
    padding-right: 2%;
    padding-left: 2%;

}

.endpoint {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 5px;
    color: white;
    padding-right: 2%;
    padding-left: 2%;
    width: 200px;
}

.description {
    margin-top: 5px;
    font-size: 0.9em;
    color: #888;

}

.highlighted {
    background-color: yellow;
}
</style>
