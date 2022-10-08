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
                    <v-card-title class="text-h5 text-md-h6 text-sm-subtitle-1 text-xs-subtitle-1">المعلم/
                        {{teacher.name}}</v-card-title>

                    <v-card-text class="text-start">{{teacher.about}}</v-card-text>

                    <v-card-actions>
                        <v-btn text color="teal accent-4" @click="reveal = true">
                            المزيد...
                        </v-btn>
                    </v-card-actions>

                    <v-expand-transition>
                        <v-card v-if="reveal" :color="teacher.color" class="transition-fast-in-fast-out v-card--reveal"
                            style="height: 100%;">
                            <v-card-text class="pb-0">
                                <p class="text-h4">
                                    عن المعلم
                                </p>
                                <p>{{teacher.fullName}}</p>
                                <p>{{teacher.description}}</p>
                            </v-card-text>
                            <v-card-actions class="pt-0">
                                <v-btn text color="teal accent-4" @click="reveal = false">
                                    أغلق
                                </v-btn>
                            </v-card-actions>
                        </v-card>
                    </v-expand-transition>


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
            reveal: false,
            teachers: [
                {
                    name: "عماد أنور",
                    fullName: "عماد أنور محمد علي الديب",
                    image: "https://i.imgur.com/ymITM4n.png",
                    about: "حاصل على درجتي الماجستير والدكتوراة في التفسير وعلوم القرآن الكريم...",
                    description: "حاصل على درجتي الماجستير والدكتوراة في التفسير وعلوم القرآن الكريم. 	مجاز بخمس إجازات قرآنية عن ظهر غيب بالسند المتصل إلى النبي ﷺ بروايات مختلفة. مجاز بالعديد من متون التجويد والقراءات من كبار مشايخ القراءات. محاضر في جامعة الإسراء بولاية مينيسوتا بأمريكا. مدرب معتمد بقسم القراءات والتجويد بالجمعية الخيرية لتحفيظ القرآن الكريم بالخبر بالمملكة العربية السعودية. ",
                    color: '#001E26',
                    yotube: "https://www.youtube.com/channel/UCZ-TqjQwQfURaDWv0VcF3CA"
                },
                {
                    name: "محمد فاروق",
                    fullName: "محمد فاروق إبراهيم",
                    image: "https://i.imgur.com/kIktEVh.png",
                    about: "حاصل على درجة الماجستير في التربية...",
                    description: "حاصل على درجة الماجستير في التربية. - مدرب معتمد بجمعية تحفيظ القرآن الكريم بالخبر بالمملكة العربية السعودية. - عمل بحلقات التحفيظ ودورات التجويد وتعليم غير الناطقين بالعربية. - مجاز بالعديد من المتون العلمية متن تحفة الأطفال ومتن المقدمة الجزرية ومتن السلسبيل الشافي",
                    color: "#001E26",
                    yotube: "https://www.youtube.com/channel/UC9cGScMGbz89eq3u2v-rjGA"
                },
                {
                    name: "أحمد فودة",
                    fullName: "أحمد بن عبد الرحمن فودة",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-3.png",
                    about: "حاصل على درجة الماجستير في التربية من الأزهر الشريف...",
                    description: "حاصل على درجة الماجستير في التربية من الأزهر الشريف. مجاز بالقراءات العشر الصغرى.  مدرب معتمد بقسم القراءات والتجويد بالجمعية الخيرية لتحفيظ القرآن الكريم بالخبر بالمملكة العربية السعودية. المشرف التعليمي بمجمع سعد بن صليب العتيبي القرآني بجامع خادم الحرمين الشريفين بالخبر. مجاز بالعديد من المتون العلمية",
                    color: "#001E26",
                    yotube: "https://www.youtube.com/channel/UCC5pdvevmhjV9syAQt_NsuQ"
                },
                {
                    name: "حافظ رضوان",
                    fullName: "حافظ عبد الله إمام رضوان",
                    image: "https://i.imgur.com/HJXCAmn.png",
                    about: "خريج معهد القراءات ومعلم القراءات بالأزهر الشريف والكبرى ومجاز بالقراءات العشر الصغرى...",
                    description: "خريج معهد القراءات بالأزهر الشريف ومعلم قراءات بالأزهر الشريف. ومجاز بالقراءات العشر الصغرى والكبرى.  ومدرب معتمد بقسم القراءات والتجويد بالجمعية الخيرية لتحفيظ القرآن الكريم بالخبر بالمملكة العربية السعودية. ومعلم القراءات بجمعية الأمير سلطان لتحفيظ القرآن الكريم ومقرأة الشاطبية. مجاز بالعديد من المتون العلمية",
                    color: "#001E26",
                    yotube: ""
                },
                {
                    name: "أحمد بركات",
                    fullName: "أحمد رجب زين الدين بركات",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-3.png",
                    about: "مجاز بقراءة عاصم بروايه حفص وشعبة ورواية ورش وأصحاب الصلة وحمزة والسوسي...",
                    description: "ليسانس دار العلوم في اللغة العربية والعلوم الإسلامية. دبلوم الدراسات العليا في علم اللغة. مجاز بقراءة عاصم براوييه حفص وشعبة ورواية ورش وأصحاب الصلة وحمزة والسوسي رحمهم الله جميعا. مدرب معتمد بجمعية تحفيظ القرآن الكريم بالخبر بالمملكة العربية السعودية. كما عمل مشرف تعليمي بحلقات جامع الإمام ابن القيم بمدينة الخبر. ديوانان في الشعر العمودي ( قطرات من ندى وغسق الدجى)",
                    color: "#001E26",
                    yotube: ""
                },
                {
                    name: "أحمد المزين",
                    fullName: "أحمد سعيد المزين",
                    image: "https://i.imgur.com/WG7EO0j.png",
                    about: "حاصل على معهد القراءات بالأزهر الشريف...",
                    description: "حاصل على معهد القراءات بالأزهر الشريف. حاصل على درجة الليسانس في القراءات وعلوم القران الكريم. مجاز بالقراءات العشر الصغرى والكبرى. مجاز بالعديد من المتون العلمية",
                    color: "#001E26",
                    yotube: ""
                },
                {
                    name: "حنان أبو الدهب",
                    fullName: "حنان أبو الدهب",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-3.png",
                    about: "مجازة بالقراءات العشر...",
                    description: "مجازة بالقراءات العشر. حاصلة على درجة الماجستير في علوم القرآن الكريم من الجامعة الإسلامية ببروكسل",
                    color: "#001E26",
                    yotube: ""
                },
                {
                    name: "عمرو فايق",
                    image: "https://t3leem.vercel.app/assets/img/owners/person-4.png",
                    about: "حاصل على عدة إجازات في القراءات...",
                    description: "حاصل على عدة إجازات في القراءات. تعليم غير الناطقين باللغة العربية",
                    color: "#001E26",
                    yotube: "https://www.youtube.com/channel/UCkRGInlEPYfI2c0K7aTorkg"
                },
            ]
        }
    }
}
</script>

<style>
.v-card--reveal {
    bottom: 0;
    opacity: 1 !important;
    position: absolute;
    width: 100%;
}
</style>