<template>
    <div style="margin: 100px;">
        <Select v-model="model1" filterable style="width:200px" prefix="ios-albums">
            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
        </Select>

        <Select v-model="model10" filterable :max-tag-count="2" multiple style="width:400px">
            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
        </Select>

        <Select v-model="model10" filterable :max-tag-count="2" multiple style="width:400px" prefix="ios-albums">
            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
        </Select>

        <br><br>

        <Select v-model="model1" style="width:200px">
            <Icon type="ios-alarm" slot="prefix" color="red" />
            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
        </Select>

        <Select v-model="model1" style="width:200px">
            <Avatar src="https://dev-file.iviewui.com/userinfoPDvn9gKWYihR24SpgC319vXY8qniCqj4/avatar" slot="prefix" size="small" />
            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
        </Select>

        <Select v-model="model10" :max-tag-count="3" :max-tag-placeholder="more" multiple style="width:400px" prefix="ios-albums">
            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
        </Select>

        <br><br>

        <Select size="small" v-model="model1" style="width:200px" prefix="ios-albums">
            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
        </Select>

        <Select size="small" v-model="model10" multiple style="width:400px" prefix="ios-albums">
            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
        </Select>

        <br><br>

        <Select size="large" v-model="model1" style="width:200px" prefix="ios-albums">
            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
        </Select>

        <Select size="large" v-model="model10" filterable multiple style="width:400px" prefix="ios-albums">
            <Option v-for="item in cityList" :value="item.value" :key="item.value" :disabled="item.disabled">{{ item.label }}</Option>
        </Select>
        <Select size="large" v-model="model10" filterable multiple style="width:400px" prefix="ios-albums">
            <OptionGroup v-for="prov in provinces" :key="prov.name" :label="prov.name">
                <Option v-for="item in prov.cityList" :value="item.value" :key="item.value" :disabled="item.disabled">{{ item.label }}</Option>
            </OptionGroup>
        </Select>
    </div>
</template>
<script>
    export default {
        data () {
            return {
                provinces: [{
                    name: 'hebei',
                    cityList: [{
                        value: 'New York',
                        label: 'New York',
                        disabled: true
                    },
                    {
                        value: 'London',
                        label: 'London'
                    }]
                },{
                    name: 'henan',
                    cityList: [{
                        value: 'Sydney',
                        label: 'Sydney',
                        disabled: true
                    },
                    {
                        value: 'Ottawa',
                        label: 'Ottawa'
                    }]
                },{
                    name: 'shandong',
                    cityList: [{
                        value: 'Paris',
                        label: 'Paris'
                    },
                    {
                        value: 'Canberra',
                        label: 'Canberra'
                    }]
                }],
                cityList: [
                    {
                        value: 'New York',
                        label: 'New York',
                        disabled: true
                    },
                    {
                        value: 'London',
                        label: 'London'
                    },
                    {
                        value: 'Sydney',
                        label: 'Sydney',
                        disabled: true
                    },
                    {
                        value: 'Ottawa',
                        label: 'Ottawa'
                    },
                    {
                        value: 'Paris',
                        label: 'Paris'
                    },
                    {
                        value: 'Canberra',
                        label: 'Canberra'
                    }
                ],
                model1: '',
                model10: ['London', 'Sydney']
            }
        },
        methods: {
            more (num) {
                return 'more' + num;
            }
        }
    }
</script>
