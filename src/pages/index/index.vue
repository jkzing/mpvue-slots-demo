<template>
  <div class="container">

    <div class="userinfo" @click="clickHandle">
      <card :text="foo"></card>
      <CompA></CompA>
    </div>
  </div>
</template>

<script>
import card from '@/components/card'
import CompA from '@/components/CompA'

export default {
  data () {
    return {
      motto: 'Hello World',
      userInfo: {},
      foo: Date.now()
    }
  },

  components: {
    card,
    CompA
  },

  methods: {
    clickHandle (msg, ev) {
      console.log('clickHandle:', msg, ev)
      this.foo = Date.now()
    }
  }
}
</script>

<style scoped>
.userinfo {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.userinfo-avatar {
  width: 128rpx;
  height: 128rpx;
  margin: 20rpx;
  border-radius: 50%;
}

.userinfo-nickname {
  color: #aaa;
}

.usermotto {
  margin-top: 150px;
}

.form-control {
  display: block;
  padding: 0 12px;
  margin-bottom: 5px;
  border: 1px solid #ccc;
}

</style>
