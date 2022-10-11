<template>
    <section class="members">
        <h2 class='mb-5 py-3'>هيئة التدريس</h2>
        <v-row justify="center">
            <v-col v-for="(teacher, i) in teachers" :key="i" cols="12" sm="8" md="5" lg="4" xl="3" align-self="center">
                <v-card class="teacher__card mx-auto my-6 px-1" mx-width="374" dark>
                    <template slot="progress">
                        <v-progress-linear color="deep-purple" height="10" indeterminate></v-progress-linear>
                    </template>

                    <div class="text-center">
                        <v-avatar class="ma-3" size="135" tile>
                            <v-img class="mx-auto rounded-circle" :src="teacher.image"></v-img>
                        </v-avatar>
                    </div>

                    <v-card-title class="justify-center text-h5 text-md-h6 text-sm-subtitle-1 text-xs-subtitle-1">
                        {{teacher.title}}/ {{teacher.name}}
                    </v-card-title>

                    <v-card-text class="text-start">{{teacher.about}}</v-card-text>

                    <v-divider class="mx-4"></v-divider>

                    <v-btn v-if="teacher.yotube === ''" icon>
                        <v-icon></v-icon>
                    </v-btn>

                    <v-btn v-else icon :href="teacher.yotube" target="_blank">
                        <v-icon large style="color: rgb(255,0,0)">
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
            reveal: false,
            teachers: [
                {
                    name: "عماد الديب",
                    title: "الدكتور",
                    fullName: "عماد أنور محمد علي الديب",
                    image: "https://i.imgur.com/ymITM4n.png",
                    about: "محاضر في جامعة الإسراء بولاية مينيسوتا بامريكا - مشرف قناة النبأ العظيم",
                    yotube: "https://www.youtube.com/channel/UCZ-TqjQwQfURaDWv0VcF3CA"
                },
                {
                    name: "حنان أبو الدهب",
                    title: "الدكتورة",
                    fullName: "حنان أبو الدهب",
                    image: "https://cdn-icons-png.flaticon.com/512/921/921107.png",
                    about: "حاصلة على درجة الماجستير في علوم القرآن الكريم من الجامعة الإسلامية ببروكسل",
                    yotube: ""
                },
                {
                    name: "حافظ رضوان",
                    title: "فضيلة الشيخ المقرئ",
                    fullName: "حافظ عبد الله إمام رضوان",
                    image: "https://i.imgur.com/HJXCAmn.png",
                    about: "معلم القراءات بجمعية الأمير سلطان لتحفيظ القرآن الكريم ومقرأة الشاطبية",
                    yotube: ""
                },
                {
                    name: "أحمد المزين",
                    title: "فضيلة الشيخ المقرئ",
                    fullName: "أحمد سعيد المزين",
                    image: "https://i.imgur.com/WG7EO0j.png",
                    about: "حاصل على ليسانس كلية القرآن الكريم للقراءات وعلومها معلم القرآن الكريم في أكاديمية مدكر  وإتقان",
                    yotube: ""
                },
                {
                    name: "أحمد فودة",
                    title: "فضيلة الشيخ المقرئ",
                    fullName: "أحمد بن عبد الرحمن فودة",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-3.png",
                    about: "المشرف التعليمي بمجمع سعد العتيبي القرآني بجامع خادم الحرمين الشريفين",
                    yotube: "https://www.youtube.com/channel/UCC5pdvevmhjV9syAQt_NsuQ"
                },
                {
                    name: "محمد فاروق",
                    title: "الأستاذ",
                    fullName: "محمد فاروق إبراهيم",
                    image: "https://i.imgur.com/kIktEVh.png",
                    about: "معلم التجويد للناطقين بغير العربية - مؤسس اكاديمية مكة المكرمة",
                    yotube: "https://www.youtube.com/channel/UC9cGScMGbz89eq3u2v-rjGA"
                },
                {
                    name: "أحمد بركات",
                    title: "الأستاذ",
                    fullName: "أحمد رجب زين الدين بركات",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-3.png",
                    about: "مجاز بقراءة عاصم بروايه حفص وشعبة ورواية ورش وأصحاب الصلة وحمزة والسوسي...",
                    yotube: ""
                },
                {
                    name: "عمرو أحمد فايق",
                    title: "الأستاذ",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-4.png",
                    about: "مشرف موقع أكاديمية مكة المكرمة ومعلم نور البيان للناطقين بغير العربية بالأكاديمية",
                    color: "#001E26",
                    yotube: "https://www.youtube.com/channel/UCkRGInlEPYfI2c0K7aTorkg"
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.v-card--reveal {
    bottom: 0;
    opacity: 1 !important;
    position: absolute;
    width: 100%;
}

.teacher__card {
    border-color: #088837 #088837 #007827 !important;
    background-color: #29b35b !important;
    background: linear-gradient(180deg, #2ec866, #084b20) !important;
}
</style>