<template>
    <v-app>
        <div class="layout">
            <Layout>
                <Head></Head>
                <Layout>
                    <Sider hide-trigger>
                        <Left></Left>
                    </Sider>
                     <Layout>
                        <Content :style="{padding: '24px', minHeight: '280px', background: '#fff'}">
                            <router-view></router-view>
                        </Content>
                    </Layout>
                </Layout>
                <Foot></Foot>
            </Layout>
        </div>
    </v-app>
</template>
<script>
import Left from "@/components/layout/left";
import Head from "@/components/layout/header";
import Footer from "@/components/layout/footer";
export default {
  data() {
    return {
       
    };
  },
  components: {
    Left: Left,
    Head: Head,
    Foot: Footer
  },
  computed: {},
  methods: {}
};
</script>

<style scoped>

.layout{
    border: 1px solid #d7dde4;
    background: #f5f7f9;
    position: relative;
    border-radius: 0px;
    overflow: hidden;
}
.layout-logo{
    width: 100px;
    height: 30px;
    background: #5b6270;
    border-radius: 3px;
    float: left;
    position: relative;
    top: 15px;
    left: 20px;
}
</style>