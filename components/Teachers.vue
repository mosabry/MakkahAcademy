<template>
    <section class="members">
        <h2 class='mb-5 py-3'>هيئة التدريس</h2>
        <v-row justify="center">
            <v-col v-for="(teacher, i) in teachers" :key="i" cols="12" sm="8" md="5" lg="4" xl="3" align-self="center">
                <v-card :color="teacher.color" class="mx-auto my-6 px-1" mx-width="374" dark>
                    <template slot="progress">
                        <v-progress-linear color="deep-purple" height="10" indeterminate></v-progress-linear>
                    </template>

                    <div class="text-center">
                        <v-avatar class="ma-3" size="135" tile>
                            <v-img class="mx-auto rounded-circle" :src="teacher.image"></v-img>
                        </v-avatar>
                    </div>
                    <v-card-title class="text-h5 text-md-h6 text-sm-subtitle-1 text-xs-subtitle-1">المعلم/ {{teacher.name}}</v-card-title>

                    <v-card-text class="text-start">{{teacher.about}}</v-card-text>

                    <v-divider class="mx-4"></v-divider>
                    <v-btn v-if="teacher.yotube === ''" icon>
                        <v-icon></v-icon>
                    </v-btn>

                    <v-btn v-else icon :href="teacher.yotube" target="_blank">
                        <v-icon style="color: #fff">
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
                    image: "https://i.imgur.com/ymITM4n.png",
                    about: "حاصل على درجتي الماجستير والدكتوراة في التفسير وعلوم القرآن الكريم. مدرب معتمد بقسم القراءات والتجويد بالجمعية الخيرية لتحفيظ القرآن الكريم بالخبر بالمملكة العربية السعودية",
                    color: '#1DA39A',
                    yotube: "https://www.youtube.com/channel/UCZ-TqjQwQfURaDWv0VcF3CA"
                },
                {
                    name: "محمد فاروق",
                    image: "https://i.imgur.com/kIktEVh.png",
                    about: "حاصل على درجة الماجستير في التربية. مدرب معتمد بجمعية تحفيظ القرآن الكريم بالخبر بالمملكة العربية السعودية",
                    color: "#1DA39A",
                    yotube: "https://www.youtube.com/channel/UC9cGScMGbz89eq3u2v-rjGA"
                },
                {
                    name: "أحمد فودة",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-3.png",
                    about: "حاصل على درجة الماجستير في التربية من الأزهر الشريف. المشرف التعليمي بمجمع سعد بن صليب العتيبي القرآني بجامع خادم الحرمين الشريفين بالخبر",
                    color: "#1DA39A",
                    yotube: "https://www.youtube.com/channel/UCC5pdvevmhjV9syAQt_NsuQ"
                },
                {
                    name: "حافظ رضوان",
                    image: "https://i.imgur.com/HJXCAmn.png",
                    about: "خريج معهد القراءات ومعلم القراءات بالأزهر الشريف والكبرى ومجاز بالقراءات العشر الصغرى. ومدرب معتمد بقسم القراءات والتجويد بالجمعية الخيرية لتحفيظ القرآن الكريم بالخبر بالمملكة العربية السعودية",
                    color: "#2E7D32",
                    yotube: ""
                },
                {
                    name: "أحمد بركات",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-3.png",
                    about: "مجاز بقراءة عاصم بروايه حفص وشعبة ورواية ورش وأصحاب الصلة وحمزة والسوسي. مدرب معتمد بجمعية تحفيظ القرآن الكريم بالخبر بالمملكة العربية السعودية",
                    color: "#2E7D32",
                    yotube: ""
                },
                {
                    name: "أحمد المزين",
                    image: "https://i.imgur.com/WG7EO0j.png",
                    about: "حاصل على معهد القراءات بالأزهر الشريف. حاصل على درجة الليسانس في القراءات وعلوم القران الكريم. مجاز بالقراءات العشر الصغرى والكبرى والعديد من المتون العلمية",
                    color: "#2E7D32",
                    yotube: ""
                },
                {
                    name: "حنان أبو الدهب",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-3.png",
                    about: "مجازة بالقراءات العشر. حاصلة على درجة الماجستير في علوم القرآن الكريم من الجامعة الإسلامية ببروكسل ",
                    color: "#2E7D32",
                    yotube: ""
                },
                {
                    name: "عمرو فايق",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-4.png",
                    about: "حاصل على عدة إجازات في القراءات. اجادة التعليم باللغة الانجليزية",
                    color: "#2E7D32",
                    yotube: "https://www.youtube.com/channel/UCkRGInlEPYfI2c0K7aTorkg"
                },
            ]
        }
    }
}
</script>