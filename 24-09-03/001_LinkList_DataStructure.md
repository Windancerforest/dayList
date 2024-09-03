# Data Structure



## LinkList

### Constructor

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
        this.length = 1;
    }

    //Push Method
    push(value){
    const newNode = new Node(value);
    if(!this.head){
        this.head=newNode;
        this.tail=newNode;        
    } else{
        this.tail.next = newNode;
        this.tail = newNode;
    }
    this.length++;
    return this;
    }
}

```

### Push Method

```javascript
push(value){
    const newNode = new Node(value);
    if(!this.head){
        this.head=newNode;
        this.tail=newNode;        
    } else{
        this.tail.next = newNode;
    }
    this.length++;
    return this;
}
```

### Pop Method

```javascript
pop(){
    if(!this.head{
    return undefined;
    }else {
        let temp=this.head;
        let pre=this.head;
        while(temp.next){
            pre=temp;
            temp=temp.next;
        }
        this.tail=pre;
        this.tail.next=null;
        this.length--;
        if(this.length==0){
            this.head=null;
            this.tail=null;
        }
    }
    return temp;
}
```
