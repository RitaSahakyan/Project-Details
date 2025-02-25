<template>
    <div class="description container">
        <div class="description_heading">{{ descriptionHeading }}</div>
        <p class="description_heading_textfirst">{{ descriptionTextFirst }}</p>
        <p class="description_heading_textsecond">{{ descriptionTextSecond }}</p>
    </div>
</template>

<script>
import { mapState } from 'vuex';

export default {
    name: "DescriptionComponent",
    computed: {
        ...mapState(["descriptionHeading", "descriptionTextFirst", "descriptionTextSecond"])
    }
};
</script>

<style>
.description{
    margin-top: 200px;
    margin-bottom: 103px;
    width: 658px;
    margin-left: 271px;
}
.description_heading{
    font-size: 50px;
    line-height: 125%;
    color: #292F36;
    margin-bottom: 11px;
    width: 565px;
}
.description_heading_textfirst{
    font-size: 22px;
    line-height: 150%;
    color: #4D5053;
    margin-bottom: 30px;
}
.description_heading_textsecond{
    font-size: 22px;
    line-height: 150%;
    color: #4D5053;
}
</style>
