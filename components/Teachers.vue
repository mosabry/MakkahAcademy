<template>
    <section class="members">
        <h2 class='mb-5 py-3'>هيئة التدريس</h2>
        <v-row justify="center">
            <v-col v-for="(Teacher, i) in Teachers" :key="i" xs="12" sm="8" md="3">
                <v-card :color="Teacher.color" class="mx-auto my-12" mx-width="374" dark>
                    <template slot="progress">
                        <v-progress-linear color="deep-purple" height="10" indeterminate></v-progress-linear>
                    </template>

                    <v-avatar class="ma-3" size="125" tile>
                        <v-img :src="Teacher.image"></v-img>
                    </v-avatar>

                    <v-card-title class="text-h5" v-text="Teacher.name"></v-card-title>

                    <v-crad-text>{{Teacher.about}}</v-crad-text>

                </v-card>
            </v-col>
        </v-row>
    </section>
</template>

<script>
export default {
    data() {
        return {
            Teachers: [
                {
                    name: "الشيخ عماد",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-1.png",
                    about: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In vehicula dui bibendum nunc cursus, in.",
                    color: '#1F7087',
                },
                {
                    name: "الشيخ محمد فاروق",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-2.png",
                    about: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In vehicula dui bibendum nunc cursus, in.",
                    color: "#00DC82",
                },
                {
                    name: "الشيخ أحمد فودة",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-3.png",
                    about: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In vehicula dui bibendum nunc cursus, in.",
                    color: "#00DC82",
                },
                {
                    name: "الشيخ عمرو فايق",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-4.png",
                    about: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In vehicula dui bibendum nunc cursus, in.",
                    color: "#00DC82",
                },
            ]
        }
    }
}
</script>