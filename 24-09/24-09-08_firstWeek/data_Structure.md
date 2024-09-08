# Data Structure JavaScript

## LinkList

### Constructure

```javascript
class Node {
    constructor (value){
        this.value=value;
        this.next=null;
    }
}

class LinkedList {
    constructor(value){
        const newNode = new Node(value);
        this.head = newNode;
        this.tail = this.head;
        this.lengt
        h = 1;
    }
}
```

### Push

```javascript
push(value){
    const newNode = new Node(value);
    if(!this.head){
        this.head = newNode;
        this.tail = newNode;        
    } else{
        this.tail.next = newNode;
        this.tail = newNode;
    }
    this.length++;
    return this;
    }
```

### Unshift

```javascript
unshift(value){
    const newNode= new Node(value);
    if(!this.head){
        this.head=newNode;
        this.tail=newNode;
    }
    else{
        newNode.tail=this.head;
        this.head=newNode;
    }
    this.length++;
    return this;
}
```

### Shift

```javascript
shift(){
    if(!this.head) return undefined;
    let temp=this.head;
    this.head=this.head.next;
    temp.next=null;
    this.length--;
    if(this.length===0){
    this.tail=null;
    }
    return temp;
}
```

### Get

```javascript
get(index){
    if(index<0||index>=this.length){
        return undefined;
    }
    let temp=this.head;
    for(leti=0;i<index;i++){
    temp=temp.next;
    }
    return temp;
}
```

### Set

```javascript
set(index,value){
    if(this.get(index)){
        this.get(index).value=value;
    }else{
        return undefined;
    }
}
```
