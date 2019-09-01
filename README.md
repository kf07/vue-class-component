# vue-class-component

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## Dataの定義
コンポーネントのDataを定義するためには、クラスメンバーとして値を宣言する  
TypeScriptの型定義をそのまま使える。初期値の代入もここで行う
```typescript
export default class HelloWorld extends Vue {
  flag: boolean = false
  inputText: string | null = null
  bounds: ClientRect | DOMRect | null = null
}
```

##  Prop
@Propデコレーターを使用してクラスメンバーとして宣言  
初期値はdefaultで付与  
@Propのクラスメンバー宣言をする際には、名称に続けて「！」キーワードが必要
```typescript
export default class HelloWorld extends Vue {
  @Prop({ type: Boolean, default: false})
  flag!: boolean
  
  @Prop({ type: [String,Number],default :null})
  message!: string | null
  
  @Prop({ type: [String, Number], default: null })
  value!: string | number | null
}
```

## computed
computedはgetを使用
```typescript
export default class HelloWorld extends Vue {
  name: string = 'Taro'

  get greet(): string {
    return `Hello ${this.name}`
  }
}
```