<template>
    <div class="container">
        <div class="firstSection">
            <div class="title">Post Trucks</div>
            <div class="buttons">
                <div class="play">Play</div>
                <div class="addNew" @click="isActive = !isActive">Add New</div>
                <div class="deleteAll">Delete All </div>
                <div class="repostAll">Repost All</div>
            </div>
            <div class="tracksList">
                <div class="trackListHeading">
                    <ul>
                        <li>Call Controll</li>
                        <li>Read</li>
                        <li>Sound / Auto Call</li>
                        <li>Truck</li>
                        <li>Origin</li>
                        <li>Destination</li>
                        <li>Pickup</li>
                        <li>DH-O</li>
                        <li>DH-D</li>
                        <li>F/P</li>
                        <li>Destination</li>
                        <li>Length</li>
                        <li>Weight</li>
                        <li>Trip/li>
                        <li>Alarm</li>
                        <li>Actions</li>
                    </ul>
                </div>
                <div class="tracks"></div>
            </div>
        </div>
        <search-section></search-section>
    </div>
</template>

<script>
    import Search from "./components/Search.vue";


    export default {
        data() {
            return {
                isActive: false,
                tracks:[
                    {
                        callControll: true,
                        read: "",
                        sound: "",
                        truck: "First",
                        origin: "",
                        destination: "",
                        pickup:"",
                        dho:371,
                        dhp: "",
                        fp:"F",
                        length:"",
                        weight:"",
                        trip:422,
                        alarm:"",
                        actions:""
                    },
                    {
                        callControll: true,
                        read: "",
                        sound: "",
                        truck: "Second",
                        origin: "",
                        destination: "",
                        pickup:"",
                        dho:371,
                        dhp: "",
                        fp:"F",
                        length:"",
                        weight:"",
                        trip:422,
                        alarm:"",
                        actions:""
                    },
                    {
                        callControll: true,
                        read: "",
                        sound: "",
                        truck: "Third",
                        origin: "",
                        destination: "",
                        pickup:"",
                        dho:371,
                        dhp: "",
                        fp:"F",
                        length:"",
                        weight:"",
                        trip:422,
                        alarm:"",
                        actions:""
                    },

                ]
            }
        },
        components:{
            "search-section":Search
        }
    }



</script>

<style>
    body{
        background-color: #C6DBEC;
    }
    .container{
        width: 95%;
        margin: 0 auto;
    }
    .play,.addNew, .deleteAll, .repostAll{
        display: inline-block;
    }
    .trackListHeading ul{
        display: inline-block;
        list-style-type: none;
        margin: 0;
        padding: 0;
        border: 1px solid white;
        background-color: #434142;
        color: white;
    }
    .trackListHeading ul li{
        border-bottom: 1px solid white;
        padding: 3px;
        line-height: 2;
    }
    .trackListHeading ul li:last-child{
        border-bottom: none;
    }
    .undo, .clear{
        display: inline-block;
    }
    .searchTracksList{
        clear: both;
    }
    .searchTrackListHeading ul{
        display: inline-block;
        list-style-type: none;
        margin: 0;
        padding: 0;
        border: 1px solid white;
        background-color: #434142;
        color: white;
    }
    .searchTrackListHeading ul li{
        border-bottom: 1px solid white;
        padding: 3px;
        line-height: 2;
    }
    .searchTrackListHeading ul li:last-child{
        border-bottom: none;
    }

    @media screen and (min-width: 987px) {/*BIG*/
        .trackListHeading ul li{
            display: inline;
            border-bottom: none;
            border-right: 1px solid white;
        }
        .trackListHeading ul li:last-child {
            border-right: none;
        }
        .secondSection .title{
            float:left;
        }
        .secondSection .buttons{
            float: right;
        }
        .searchTrackListHeading ul li{
            display: inline;
            border-bottom: none;
            border-right: 1px solid white;
        }
        .searchTrackListHeading ul li:last-child {
            border-right: none;
        }
    }
    @media screen and (max-width: 319px) {/*SMALLEST*/
        .container {
            min-width: 319px;
            overflow: auto;
        }
    }
    @media screen and (min-width: 1281px) {/*BIGGEST*/
        .container {
            max-width: 1280px;
        }
    }
</style>