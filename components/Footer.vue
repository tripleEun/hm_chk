<template>
  <div>
    <footer>
        <div class="footer__container page__inner">
            <div class="sitemap">
                <div class="sitemap__container">
                    <ul class="sitemap__wrapper">
                        <li>
                            <dl>
                                <dt class="point">{{ company.menu }}</dt>
                                <dd>
                                    <div v-for="name in company.items" :key="name.index">
                                        <router-link :to="name.href">{{ name.item }}</router-link>
                                    </div>
                                </dd>
                            </dl>
                        <li>
                            <dl>
                                <dt class="point">{{ service.menu }}</dt>
                                <dd>
                                    <div v-for="name in service.items" :key="name.index">
                                        <router-link :to="name.href">{{ name.item }}</router-link>
                                    </div>
                                </dd>
                            </dl>
                        </li>
                        <li>
                            <dl>
                                <dt class="point">{{ support.menu }}</dt>
                                <dd>
                                    <div v-for="name in support.items" :key="name.index">
                                        <router-link :to="name.href">{{ name.item }}</router-link>
                                    </div>
                                </dd>
                            </dl>
                        </li>
                        <li>
                            <dl>
                                <dt class="point">{{ sns.menu }}</dt>
                                <dd>
                                    <div v-for="name in sns.items" :key="name.index">
                                        <router-link :to="name.href">{{ name.item }}</router-link>
                                    </div>
                                </dd>
                            </dl>
                        </li>

                    </ul>
                </div>
            </div>            
            <div class="company">
                <div class="company__text">
                    <span>주식회사 케이엘  대표자 (성명) : 이길원</span> 
                    <span>주소 : 경기도 용인시 수지구 풍덕천로 190번길 25 신건프라자 7층</span><br/>
                    <span>고객센터 : 1522 - 5401 ( 운영시간 : 09:00 ~ 18:00 )</span>
                    <span>사업자 등록 번호 안내 : [ 889 - 86 - 00580 ]</span><br/>
                    <span>계좌 번호 : 국민은행 390401-04-128389, 649701-01-266825, 649701-01-285811</span><br/>
                    <span>( 입금자 명 : 주식회사 케이엘 )</span><br/><br/>
                    Copyright ⓒ HomeCheck. All Rights Reserved.
                </div>
                <ul class="company__link">
                    <li>
                        <a href="javascript:;">
                            <img src="../asset/img/family_kakao.png" alt="">
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                            <img src="../asset/img/family_naver.png" alt="">
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                            <img src="../asset/img/family_youtube.png" alt="">
                        </a>
                    </li>
    
                </ul>
            </div>

        </div>
    </footer>
  </div>

</template>

<script>
import company from '@/static/company.json';
import service from '@/static/service.json';
import support from '@/static/support.json';
import sns from '@/static/sns.json';

export default {
    data() {
        return {
            company, service, support, sns
        }
    }
}
</script>

<style>

</style>