# `Stack Data Structure`

The `Stack` data structure is a sequential collection of elements that follows the principle of `Last In First Out (LIFO)`. The last element inserted into the `Stack` is first element to be removed.

The `Stack` data structure supports two main operations:

1. `Push`, which `adds` an element to the collections.

2. `Pop`, which `removes` the most recently added element from the collection.

![stack](https://camo.githubusercontent.com/e42a7be3b3183ceb983e25c44606a274f6a253b4762ce4857c5c69ed77e29e1d/68747470733a2f2f7777772e73697465736261792e636f6d2f646174612d7374727563747572652f696d616765732f707573682d6f7065726174696f6e2e676966)

![stack image](https://jojozhuang.github.io/assets/images/algorithm/1112/stack.png)

## Stack Data Structure Implementation

1. `push(element)` -> add an element to the top  of the `Stack`.

````JavaScript
     push(element){
        this.items.push(element);
    }
````

2. `pop()` -> remove the top element from the `Stack`.

````JavaScript
    pop(){
        return this.items.pop();
    }    
````

3. `peek()` -> get the value of the top element without removing it.

 ````JavaScript
     peek(){   
        return this.items[this.items.length - 1];
    }
````

4. `isEmpty()` -> check if the `Stack` is empty.

 ````JavaScript
     isEmpty(){
        return this.items.length === 0;
    }
````

5. `size()` -> get the number of element in the `Stack`.

 ````JavaScript
  size(){
        return this.items.length;
    }
````

6. `print()` -> visualize the element in the the `Stack`

````JavaScript
  print(){
        console.log(this.items.toString());
    }
````    


  


## `References`

- [YouTube](https://www.youtube.com/watch?v=a1fyufVlLmk&list=PLC3y8-rFHvwg6nsAOfC5Is18KB2DrVOJy&index=6)
- [YouTube](https://www.youtube.com/watch?v=SbjATifB2M8&list=PLC3y8-rFHvwg6nsAOfC5Is18KB2DrVOJy&index=7)

- [YouTube](https://www.youtube.com/watch?v=wjI1WNcIntg&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8&index=3&)

- [Wikipedia](https://en.wikipedia.org/wiki/Stack_(abstract_data_type))