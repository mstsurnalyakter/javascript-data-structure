# Circular Queue Data Structure

````
A Circular Queue is an extended version of a normal queue where the last element of the queue is connected to the first element of the queue forming a circle. 
````

The `Circular of Queue` data structure support two main operation:

1. `Enqueue` -> which adds an element to rear of the collection

2. `Dequeue` -> whcih removes an element from the front of the collection



![](https://media.geeksforgeeks.org/wp-content/uploads/Circular-queue.png)

![](https://media.geeksforgeeks.org/wp-content/uploads/Circular-queue_1.png)

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSb53ItCFYUTS95Xis8q-K_fkWSuhCEy37bkw&usqp=CAU)

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRHyT9Erh3aKrlNiCz7-XZ-pKsb9wGydVFHct9pLnSK4QnX8Eu5wTXIgu3_NFyL-XEOoq8&usqp=CAU)

## `Circural Queue Data Structure Implementation`

1. `enqueue(element)` -> add an element to the queue.

````JavaScript
  enqueue(element){
        if(!this.isFull()){

            this.rear = (this.rear + 1) % this.capacity;
            this.items[this.rear] = element;
            this.currentLength += 1;

            if(this.front === -1){
                this.front = this.rear;
            }
        }
    }
````

2. `dequeue()` -> remove the oldest element from the queue.

````JavaScript
  dequeue(){
        if(this.isEmpty()){
            return null;
        }

        const item = this.items[this.front];
        this.items[this.front] = null;
        this.front = (this.front + 1) % this.capacity;
        this.currentLength -= 1;

        if(this.isEmpty()){
            this.front = -1;
            this.rear = -1;
        }
        return item;
    }
````

3. `isFull()` -> check if the queue is full.

````JavaScript
    isFull(){
        return this.currentLength === this.capacity;
    }
````

4. `isEmpty()` -> check if the queue is empty.

````JavaScript
 isEmpty(){
        return this.currentLength === 0;
 }
````

5. `peek()` -> get the value of the element at the front of the queue without removing it.

````JavaScript
    peek(){
        if(!this.isEmpty()){
            return this.items[this.front];
        }

        return null;
    }
````

6. `print()` -> visualize the element in the queue.

````JavaScript
 print(){
        if(this.isEmpty()){
            console.log(`Queue is empty`);
        }else{
            let i;
            let str = '';

            for(i = this.front; i !== this.rear; i = (i + 1) % this.capacity){
                str += this.items[i] + "";
            }

            str += this.items[i];
            console.log(str);
        }
    }
````


## References

- [YouTube](https://www.youtube.com/watch?v=ngNJps_RUg8&list=PLC3y8-rFHvwg6nsAOfC5Is18KB2DrVOJy&index=11)

- [YouTube](https://www.youtube.com/watch?v=oIR_DOOOACk&list=PLC3y8-rFHvwg6nsAOfC5Is18KB2DrVOJy&index=12)


