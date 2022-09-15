<script lang="ts" setup>
import { ref } from 'vue'
import { TBox, TSpacer, TText } from '@temir/core'
import TLink from '@temir/link'
const count = ref(0)
setInterval(() => {
  count.value++
}, 10 * 1000)
</script>

<template>
  <TBox
    :margin="5"
    :width="30"
    :min-height="10"
    border-style="double"
    justify-content="center"
    align-items="center"
    flex-direction="column"
  >
    <TText bold italic underline color="black" background-color="green">
      I am black on green
    </TText>
    <TBox :padding="1" border-style="classic" border-color="green">
      <TText color="#42b883">
        🌈 Hi TEMIR !! {{ count }}
      </TText>
    </TBox>
  </TBox>
  <TBox flex-direction="column" :height="10" border-style="double" border-color="greenBright">
    <TText>Top</TText>
    <TSpacer />
    <TText>Bottom</TText>
  </TBox>

  <TBox flex-direction="row" :height="10" border-style="double" border-color="yellowBright">
    <TText>Left</TText>
    <TSpacer />
    <TText>Right</TText>
    <TLink url="https://github.com">
      <TText color="yellow">
        Hi
      </TText>
      <TText color="cyan">
        Github
      </TText>
    </TLink>
  </TBox>
</template>
