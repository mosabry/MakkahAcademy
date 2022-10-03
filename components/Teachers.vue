<template>
    <section class="members">
        <h2 class='mb-5 py-3'>هيئة التدريس</h2>
        <v-row justify="center">
            <v-col v-for="(teacher, i) in teachers" :key="i" xs="12" sm="10" md="5" lg="3">
                <v-card :color="teacher.color" class="mx-auto my-12" mx-width="374" dark>
                    <template slot="progress">
                        <v-progress-linear color="deep-purple" height="10" indeterminate></v-progress-linear>
                    </template>

                    <v-avatar class="ma-3" size="125" tile>
                        <v-img class="rounded-circle" :src="teacher.image"></v-img>
                    </v-avatar>

                    <v-card-title class="text-h5">الشيخ/ {{teacher.name}}</v-card-title>

                    <v-crad-text>{{teacher.about}}</v-crad-text>

                    <v-divider class="mx-4"></v-divider>

                    <v-btn icon :href="teacher.yotube" target="_blank">
                        <v-icon large style="color: #FF0000">
                            mdi-youtube
                        </v-icon>
                    </v-btn>

                </v-card>
            </v-col>
        </v-row>
    </section>
</template>

<script>
export default {
    data() {
        return {
            teachers: [
                {
                    name: "عماد أنور",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-1.png",
                    about: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In vehicula dui bibendum nunc cursus, in.",
                    color: '#1F7087',
                    yotube: "https://www.youtube.com/channel/UCZ-TqjQwQfURaDWv0VcF3CA"
                },
                {
                    name: "محمد فاروق",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-2.png",
                    about: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In vehicula dui bibendum nunc cursus, in.",
                    color: "#1F7087",
                    yotube: "https://www.youtube.com/channel/UC9cGScMGbz89eq3u2v-rjGA"
                },
                {
                    name: "أحمد فودة",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-3.png",
                    about: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In vehicula dui bibendum nunc cursus, in.",
                    color: "#00DC82",
                    yotube: "https://www.youtube.com/channel/UCC5pdvevmhjV9syAQt_NsuQ"
                },
                {
                    name: "حافظ رضوان",
                    image: "https://i.imgur.com/HJXCAmn.png",
                    about: "خريج معهد القراءات ومعلم القراءات بالأزهر الشريف والكبرى ومجاز بالقراءات العشرى الصغرى",
                    color: "#00DC82",
                    yotube: ""
                },
                {
                    name: "عمرو فايق",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-4.png",
                    about: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In vehicula dui bibendum nunc cursus, in.",
                    color: "#00DC82",
                    yotube: "https://www.youtube.com/channel/UCkRGInlEPYfI2c0K7aTorkg"
                },
            ]
        }
    }
}
</script>