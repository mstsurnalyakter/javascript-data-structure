# `Queue Data Structure`

 
The `Queue` data structure is a sequential collection of elements that follows the principle of `First In First Out(FIFO)`. The first element inserted into the `Queue` is first element to be removed.
 

The `Queue` data structure supports `two` main operations:

1. `Enqueue` -> which add an elementto the `rear` of the collection.
2. `Dequeue` -> which `removes` an element from the `front` of the collection.

![queue](https://www.simplilearn.com/ice9/free_resources_article_thumb/Queue-Representation.png)


## `Enqueue operation`


![queque](https://www.simplilearn.com/ice9/free_resources_article_thumb/Queue_in_Data_Structure-Enqueue_Operation.png)

## `Dequeue operation`


![queue](https://www.simplilearn.com/ice9/free_resources_article_thumb/Queue_in_Data_Structure-Dequeue_Operation.png)


## Queue Data Structure Implementation

 


1. `enqueue(element)` -> add an element to queue.

````JavaScript
    enqueue(element){
        this.items.push(element);
    }
````

2. `dequeue()` -> remove the oldest element from the queue.

````JavaScript
    dequeue(){
        return this.items.shift();
    }
````

3. `peek()` -> get the value of the element at the front of the queue without removing it.

````JavaScript
 peek(){
        if(!this.isEmpty()){
            return this.items[0]
        }
        return null;
    }
````

4. `isEmpty()` -> check if the queue is empty.

````JavaScript
 isEmpty(){
        return this.items.length === 0;
    }
````

5. `size()` -> get the number of elements in the queue.

````JavaScript
     size(){
        return this.items.length;
    }
````

6. `print()` -> visualize the elements in the queue.

````JavaScript
 print(){
        console.log(this.items.toString());
    }
````

 



## References

- [YouTube](https://www.youtube.com/watch?v=ex8EHl5fq1o&list=PLC3y8-rFHvwg6nsAOfC5Is18KB2DrVOJy&index=8)
- [YouTube](https://www.youtube.com/watch?v=NuBWJ7kIlDg&list=PLC3y8-rFHvwg6nsAOfC5Is18KB2DrVOJy&index=9)

- [YouTube](https://www.youtube.com/watch?v=ba15sgOiAOg&list=PLC3y8-rFHvwg6nsAOfC5Is18KB2DrVOJy&index=10)

- [YouTube](https://www.youtube.com/watch?v=wjI1WNcIntg&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8&index=3&)

- [YueTube](https://youtu.be/yzj0Ch01Exo)

- [Wikipedia](https://en.wikipedia.org/wiki/Stack_(abstract_data_type))