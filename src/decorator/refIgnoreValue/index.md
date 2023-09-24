## Usage

```ts
class Test {
  // #state = ref<{ aa: number }>()

  // get state() {
  // console.log('get')
  // return this.#state.value
  // }

  // set state(val) {
  // console.log('val',val)
  // this.#state.value = val
  // }

  // repalce above usage
  @refIgnoreValue
  state2: number

  constructor() {
    this.reset()
    console.log('state', this.state1)
    this.state2 = 666
  }

  get aa() {
    return this.state1.aa
  }

  reset() {
    this.state1 = {
      aa: 1
    }
  }

  changeVal() {
    this.state1.aa = 3
  }
}
```