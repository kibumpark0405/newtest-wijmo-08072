<template>
    <wj-flex-grid
        ref="flexGridDetails"
        :autoGenerateColumns="false"
        :allowAddNew="false"
        :allowDelete="true"
        :allowPinning="'SingleColumn'"
        :newRowAtTop="false"
        :showMarquee="true"
        :selectionMode="'MultiRange'"
        :validateEdits="false"
        :itemsSource="selectedGrid"
        :initialized="flexDetailsInitialized"
        style="margin-top:10px; max-height:65vh;"
    >
        <wj-flex-grid-cell-template cellType="RowHeader" v-slot="cell">{{cell.row.index + 1}}</wj-flex-grid-cell-template>
    </wj-flex-grid>
</template>

<script>
import BaseDetailGrid from '../base-ui/BaseDetailGrid';
import SalesItem from '../SalesItem.vue';

export default {
    name: 'SalesItemsDetailGrid',
    mixins: [BaseDetailGrid],
    components: [
        SalesItem
    ],
    methods: {
    }
}
</script>

