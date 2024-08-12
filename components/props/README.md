## Props

公式ドキュメント : https://react.dev/learn/passing-props-to-a-component

コンポーネントはプロップスを受け取ることができる

```javascript
function Avatar(props) {
  return <img src={props.url} alt={props.name} />
}

export default function Profile() {
  return <Avatar url="https://john-doe.jpg" name="john doe" />
}
```

分割代入を使用してプロップ内のオブジェクトを直接使用する
```javascript
function Avatar({url, name}) {
  return <img src={url} alt={name} />
}

export default function Profile() {
  return <Avatar url="https://john-doe.jpg" name="john doe" />
}
```

### JSXを子として渡す

```javascript
function Card({ children }) {
  return (
    <div className="card">
      {children}
    </div>
  );
}

export default function Profile() {
  return (
    <Card>
      <Avatar
        size={100}
        person={{ 
          name: 'Katsuko Saruhashi',
          imageId: 'YfeOqp2'
        }}
      />
    </Card>
  );
}
```
