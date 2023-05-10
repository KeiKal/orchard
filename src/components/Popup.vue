
<template>
    <v-dialog v-model="dialogVisible" max-width="500px" v-bind:class="dataFieldClass" ref="el">
        <v-card>
            <v-card-title>
                <span class="headline">Popup Title</span>
            </v-card-title>
            <v-card-text>
                <!-- Popup content goes here -->
                <p>This is the content of the popup.</p>
            </v-card-text>
            <v-card-actions>
                <v-btn color="primary" text @click="closeDialog">Close</v-btn>
            </v-card-actions>
        </v-card>
    </v-dialog>
</template>

<script>
export default {
    data() {
        return {
            dialogVisible: false
        };
    },
    methods: {
        openDialog() {
            this.dialogVisible = true;
        },
        closeDialog() {
            this.dialogVisible = false;
        }
    },
    name : 'pop-up'
};
</script>