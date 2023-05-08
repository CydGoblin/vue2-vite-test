<template>
    <ag-grid-vue
            style="width: 500px; height: 200px"
            class="ag-theme-alpine"
            :columnDefs="columnDefs"
            :rowData="rowData"
    >
    </ag-grid-vue>
</template>

<script>
import "ag-grid-community/styles/ag-grid.css";
import "ag-grid-community/styles/ag-theme-alpine.css";
import { AgGridVue } from "ag-grid-vue";
import Rating from "./Rating.vue";

export default {
    name: "App",
    components: {
        AgGridVue,
        Rating,
    },
    setup() {
        return {
            columnDefs: [
                { headerName: "Make", field: "make" },
                { headerName: "Rating", field: "rating", cellRenderer: "Rating" },
            ],
            rowData: [
                { make: "Toyota", rating: 4 },
                { make: "Ford", rating: 1 },
                { make: "Porsche", rating: 5 },
            ],
        };
    },
};
</script>
