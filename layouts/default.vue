<template>
    <div>
        <div class="header__container page__inner">
            <div id="logo">
                <img src="../asset/img/header_logo.jpg" alt="">
                <!-- <img :src="pic"> -->
                <nuxt-link to="/">HomeCheck</nuxt-link>
                <!-- <a href="javascript:;">HomeCheck</a> -->
            </div>
            <div id="gnb">
                <nav>
                    <dl class="nav-wrapper on">
                        <dt><a class="depth01" href="javascript:;">{{ company.menu }}</a></dt>
                        <div v-for="name in company.items" :key="name.href"> 
                            <dd>
                                <ul class="depth02-wrapper">
                                    <li><router-link :to="name.href" class="depth02">{{ name.item }}</router-link></li>
                                </ul>
                            </dd>
                        </div>
                    </dl>
                    <dl class="nav-wrapper">
                        <dt><a class="depth01" href="javascript:;">{{ service.menu }}</a></dt>
                        <div v-for="name in service.items" :key="name.href">
                            <dd>
                                <ul class="depth02-wrapper">
                                    <li><router-link :to="name.href" class="depth02">{{ name.item }}</router-link></li>
                                </ul>
                            </dd>
                        </div>
                    </dl>
                    <dl class="nav-wrapper">
                        <dt><a class="depth01" href="javascript:;">{{ support.menu }}</a></dt>
                        <div v-for="name in support.items" :key="name.href">
                            <dd>
                                <ul class="depth02-wrapper">
                                    <li><router-link :to="name.href" class="depth02">{{ name.item }}</router-link></li>
                                </ul>
                            </dd>
                        </div>
                    </dl>
                    <dl class="nav-wrapper">
                        <dt><a class="depth01" href="javascript:;">{{ sns.menu }}</a></dt>
                        <div v-for="name in sns.items" :key="name.href">
                            <dd>
                                <ul class="depth02-wrapper">
                                    <li><router-link :to="name.href" class="depth02 sns-kakao" >{{ name.item }}</router-link></li>
                                </ul>
                            </dd>
                        </div>
                    </dl>
                    <dl class="nav-wrapper">
                        <dt><a class="go-business" href="javascript:;">{{ bussiness.menu }}</a></dt>
                    </dl>
                </nav>
                <ul class="easy-btns">
                    <li><a class="btn02" href="javascript:;">앱으로 전환</a></li>
                    <li><a class="btn01" href="javascript:;">상담/예약</a></li>
                </ul>
            </div>
            
        </div>
        <nuxt />
    </div>
    
</template>

<script>
import company from '@/static/company.json';
import service from '@/static/service.json';
import support from '@/static/support.json';
import sns from '@/static/sns.json';
import bussiness from '@/static/bussiness.json';
// import MainHeader from 'MainHeader'

export default {
    data() {
        return {
            // pic
            company, service, support, sns, bussiness
        }
    }
}
</script>
