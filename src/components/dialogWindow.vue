<template>
    <div class="overlay">
        <div class="dialog-box">
            <!-- header -->
            <div class="header">
                <h1 class="heading">Test</h1>
            </div>

            <!-- body -->
            <div class="body">
                <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the
                    industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type
                    and scrambled it to make a type specimen book. It has survived not only five centuries, but also the
                    leap into electronic typesetting, remaining essentially unchanged.</p>
            </div>

            <!-- footer -->
            <div class="footer">
                <button @click="emitClose" class="cancel-btn">Cancel</button>
                <button class="deactivate-btn">Deactivate</button>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
const emit = defineEmits(['close']);

const emitClose = () => {
    emit('close');
};
</script>
<style scoped>
.overlay {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.5);
    /* Dark overlay */
    display: flex;
    align-items: center;
    justify-content: center;
}

.dialog-box {
    width: 400px;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.2);
    padding: 20px;
    text-align: center;
}

.header h1 {
    margin: 0;
    font-size: 20px;
    color: #e53935;
    /* Red header color */
}

.body p {
    color: #333;
    font-size: 14px;
    margin-top: 10px;
}

.footer {
    display: flex;
    justify-content: flex-end;
    gap: 10px;
    margin-top: 20px;
}

.cancel-btn {
    padding: 8px 16px;
    background-color: #f5f5f5;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

.cancel-btn:hover {
    background-color: #e0e0e0;
}

.deactivate-btn {
    padding: 8px 16px;
    background-color: #e53935;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

.deactivate-btn:hover {
    background-color: #d32f2f;
}
</style>