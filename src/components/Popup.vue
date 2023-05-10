<template>
    <div class="text-center">
        <v-btn color="grey--text" small @click="dialog = true">
            View
        </v-btn>

        <v-dialog v-model="dialog" width="auto">
            <v-card>
                <v-card-text>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et
                    dolore magna aliqua.
                </v-card-text>
                <v-card-actions>
                    <v-btn color="grey--text" small @click="dialog = false">Close</v-btn>
                </v-card-actions>
            </v-card>
        </v-dialog>
    </div>
</template>

<script>
export default {
    data() {
        return {
            dialog: false,
        }
    },
    name: 'pop-up'
}
</script>