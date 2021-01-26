<div data-v-5e9078c0="">

# Top 14 Queues interview questions and answers in 2021.

[![ https://source.unsplash.com/collection/52661698/700x350) https://devinterview.io/)

You can check all 14 Queues interview questions here 👉 https://devinterview.io/data/queues-interview-questions

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 1\. List some Queue real-life applications

</div>

<div>

### Answer:

<div class="answer">

<div>

<div>

<div class="AnswerBody">

Queue, as the name suggests is used whenever we need to manage any group of objects in an order in which the first one coming in, also gets out first while the others wait for their turn, like in the following scenarios:

*   Serving requests on a single shared resource, like a printer, CPU task scheduling etc.
*   In real life scenario, Call Center phone systems uses Queues to hold people calling them in an order, until a service representative is free.
*   Handling of interrupts in real-time systems. The interrupts are handled in the same order as they arrive i.e First come first served.

</div>

</div>

<div class="row my-2">

<div><span>Source: <span>www.studytonight.com https://www.studytonight.com/data-structures/queue-data-structure "List some Queue real-life applications Interview Questions Source To Answer"</span></span>   </div>

</div>

</div>

</div>

</div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 2\. What is Queue?

</div>

<div>

### Answer:

<div class="answer">

<div>

<div>

<div class="AnswerBody">

A **queue** is a container of objects (a _linear_ collection) that are inserted and removed according to the first-in first-out (FIFO) principle. The process to add an element into queue is called **Enqueue** and the process of removal of an element from queue is called **Dequeue**.

</div>

</div>

<div class="row my-2">

<div><span>Source: <span>www.cs.cmu.edu https://www.cs.cmu.edu/~adamchik/15-121/lectures/Stacks%20and%20Queues/Stacks%20and%20Queues.html "What is Queue? Interview Questions Source To Answer"</span></span>   </div>

</div>

</div>

</div>

</div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 3\. What is Complexity Analysis of Queue operations?

</div>

<div>

### Answer:

<div class="answer">

<div>

<div>

<div class="AnswerBody">

*   Queues offer random access to their contents by shifting the first element off the front of the queue. You have to do this repeatedly to access an arbitrary element somewhere in the queue. Therefore, **access** is `_O_(_n_)`.
*   Searching for a given value in the queue requires iterating until you find it. So **search** is `_O_(_n_)`.
*   Inserting into a queue, by definition, can only happen at the back of the queue, similar to someone getting in line for a delicious Double-Double burger at In 'n Out. Assuming an efficient queue implementation, queue **insertion** is `_O_(_1_)`.
*   Deleting from a queue happens at the front of the queue. Assuming an efficient queue implementation, queue **deletion** is ``_O_(_1_)`.

</div>

</div>

<div class="row my-2">

<div><span>Source: <span>github.com https://github.com/tim-hr/stuff/wiki/Time-complexity:-Queues "What is Complexity Analysis of Queue operations?  Interview Questions Source To Answer"</span></span>   </div>

</div>

</div>

</div>

</div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 4\. What are some types of Queue?

</div>

<div>

### Answer:

<div class="answer">

<div>

<div>

<div class="AnswerBody">

Queue can be classified into following types:

*   **Simple Queue** - is a linear data structure in which removal of elements is done in the same order they were inserted i.e., the element will be removed first which is inserted first.

*   **Circular Queue** - is a linear data structure in which the operations are performed based on FIFO (First In First Out) principle and the last position is connected back to the first position to make a circle. It is also called **Ring Buffer**. Circular queue avoids the wastage of space in a regular queue implementation using arrays.

*   **Priority Queue** - is a type of queue where each element has a priority value and the deletion of the elements is depended upon the priority value

*   In case of **max-priority queue**, the element will be deleted first which has the largest priority value
*   In case of **min-priority queue** the element will be deleted first which has the minimum priority value.
*   **De-queue (Double ended queue)** - allows insertion and deletion from both the ends i.e. elements can be added or removed from rear as well as front end.

*   **Input restricted deque** - In input restricted double ended queue, the insertion operation is performed at only one end and deletion operation is performed at both the ends.

*   **Output restricted deque** - In output restricted double ended queue, the deletion operation is performed at only one end and insertion operation is performed at both the ends.

</div>

</div>

<div class="row my-2">

<div><span>Source: <span>www.ques10.com https://www.ques10.com/p/34997/what-are-different-types-of-queues/ "What are some types of Queue? Interview Questions Source To Answer"</span></span>   </div>

</div>

</div>

</div>

</div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 5\. Why and when should I use Stack or Queue data structures instead of Arrays/Lists?

</div>

<div>

### Answer:

<div class="answer">

<div>

<div>

<div class="AnswerBody">

Because they help manage your data in more a _particular_ way than arrays and lists. It means that when you're debugging a problem, you won't have to wonder if someone randomly inserted an element into the middle of your list, messing up some invariants.

Arrays and lists are random access. They are very flexible and also easily _corruptible_. If you want to manage your data as FIFO or LIFO it's best to use those, already implemented, collections.

More practically you should:

*   Use a queue when you want to get things out in the order that you put them in (FIFO)
*   Use a stack when you want to get things out in the reverse order than you put them in (LIFO)
*   Use a list when you want to get anything out, regardless of when you put them in (and when you don't want them to automatically be removed).

</div>

</div>

<div class="row my-2">

<div><span>Source: <span>stackoverflow.com https://stackoverflow.com/questions/2074970/stack-and-queue-why "Why and when should I use Stack or Queue data structures instead of Arrays/Lists? Interview Questions Source To Answer"</span></span>   </div>

</div>

</div>

</div>

</div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 6\. Implement a Queue using two Stacks

</div>

<div>

### Answer:

<div class="answer">

<div>

<div class="mb-2"><span class="h5">Problem</span></div>

<div>

<div class="AnswerBody">

Suppose we have two stacks and no other temporary variable. Is to possible to "construct" a queue data structure using only the two stacks?

</div>

</div>

<div>

<div class="AnswerBody">

Keep two stacks, let's call them `inbox` and `outbox`.

**Enqueue**:

*   Push the new element onto `inbox`

**Dequeue**:

*   If `outbox` is empty, refill it by popping **each** element from `inbox` and pushing it onto `outbox`
*   Pop and return the top element from `outbox`

</div>

</div>

<div>

<div class="mb-2 mt-2"><span class="h5">Complexity Analysis</span></div>

<div class="hide-small">

<div class="row no-gutters my-2 align-items-end">

<div class="col font-weight-bold text-muted">Time:</div>

<div class="col text-center">

<div class="text-muted font-weight-bold justify-content-center">Constant</div>

<div class="complexity amazing first p-1 justify-content-center shadow-text selected-complexity effect7">O(1)</div>

</div>

<div class="col disable text-center">

<div class="text-muted font-weight-bold justify-content-center">Dbl. Logarithmic</div>

<div class="complexity good p-1 justify-content-center shadow-text">O(log log n)</div>

</div>

<div class="col disable text-center">

<div class="text-muted font-weight-bold justify-content-center">Logarithmic</div>

<div class="complexity good p-1 justify-content-center shadow-text">O(log n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold  text-muted justify-content-center">Square Root</div>

<div class="complexity fair p-1 justify-content-center shadow-text ">O(√n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold  text-muted justify-content-center">Linear</div>

<div class="complexity fair p-1 justify-content-center shadow-text ">O(n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold text-muted justify-content-center">Linearithmic</div>

<div class="complexity bad p-1 justify-content-center shadow-text ">O(n log n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold  text-muted justify-content-center">Quadratic</div>

<div class="complexity terrible p-1 justify-content-center shadow-text ">_O_(_n_<sup>2</sup>)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold   text-muted justify-content-center">Exponential</div>

<div class="complexity terrible p-1 justify-content-center shadow-text ">_O_(_2_<sup>n</sup>)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold text-muted">Factorial</div>

<div class="complexity terrible last p-1 justify-content-center shadow-text ">O(n!)</div>

</div>

</div>

</div>

<div class="hide-small">

<div class="row no-gutters my-2 align-items-end">

<div class="col font-weight-bold text-muted">Space:</div>

<div class="col text-center">

<div class="text-muted font-weight-bold justify-content-center">Constant</div>

<div class="complexity amazing first p-1 justify-content-center shadow-text selected-complexity effect7">O(1)</div>

</div>

<div class="col disable text-center">

<div class="text-muted font-weight-bold justify-content-center">Dbl. Logarithmic</div>

<div class="complexity good p-1 justify-content-center shadow-text">O(log log n)</div>

</div>

<div class="col disable text-center">

<div class="text-muted font-weight-bold justify-content-center">Logarithmic</div>

<div class="complexity good p-1 justify-content-center shadow-text">O(log n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold  text-muted justify-content-center">Square Root</div>

<div class="complexity fair p-1 justify-content-center shadow-text ">O(√n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold  text-muted justify-content-center">Linear</div>

<div class="complexity fair p-1 justify-content-center shadow-text ">O(n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold text-muted justify-content-center">Linearithmic</div>

<div class="complexity bad p-1 justify-content-center shadow-text ">O(n log n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold   text-muted justify-content-center">Quadratic</div>

<div class="complexity terrible p-1 justify-content-center shadow-text ">_O_(_n_<sup>2</sup>)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold   text-muted justify-content-center">Exponential</div>

<div class="complexity terrible p-1 justify-content-center shadow-text ">_O_(_2_<sup>n</sup>)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold text-muted">Factorial</div>

<div class="complexity terrible last p-1 justify-content-center shadow-text ">O(n!)</div>

</div>

</div>

</div>

<div class="hide-large">

**Time:** <mark>O(1)</mark>

**Space:** <mark>O(1)</mark>

</div>

<div class="mt-3">

<div>

<div class="AnswerBody">

In the worst case scenario when outbox stack is empty, the algorithm pops n elements from inbox stack and pushes n elements to outbox, where n is the queue size. This gives `2*n` operations, which is `O(n)`. But when outbox stack is not empty the algorithm has `O(1)` time complexity that gives amortised `O(1)`.

</div>

</div>

</div>

</div>

<div style="font-size: 14px;">

<div class="mb-3 mt-2"><span class="h5">Implementation</span></div>

<div>

<nav class="mdc-tab-bar">

<div class="mdc-tab-scroller">

<div class="mdc-tab-scroller__scroll-area mdc-tab-scroller__scroll-area--scroll" style="margin-bottom: 0px;">

<div class="mdc-tab-scroller__scroll-content"><button class="mdc-ripple-upgraded mdc-ripple-upgraded--background-focused mdc-tab mdc-tab--min-width mdc-tab--active" aria-selected="true" tabindex="0">

<div class="mdc-tab__content"><span class="mdc-tab__text-label"><span>C#</span> <span class="shadow-text lang-badge cs">CS</span></span></div>

<span class="mdc-tab-indicator mdc-tab-indicator--active"><span aria-hidden="true" class="mdc-tab-indicator__content mdc-tab-indicator__content--underline"></span></span></button><button class="mdc-ripple-upgraded mdc-tab mdc-tab--min-width">

<div class="mdc-tab__content"><span class="mdc-tab__text-label"><span>JavaScript</span> <span class="shadow-text lang-badge js">JS</span></span></div>

<span class="mdc-tab-indicator"><span aria-hidden="true" class="mdc-tab-indicator__content mdc-tab-indicator__content--underline"></span></span></button><button class="mdc-ripple-upgraded mdc-tab mdc-tab--min-width">

<div class="mdc-tab__content"><span class="mdc-tab__text-label"><span>Java</span> <span class="shadow-text lang-badge java">Java</span></span></div>

<span class="mdc-tab-indicator"><span aria-hidden="true" class="mdc-tab-indicator__content mdc-tab-indicator__content--underline"></span></span></button><button class="mdc-ripple-upgraded mdc-tab mdc-tab--min-width">

<div class="mdc-tab__content"><span class="mdc-tab__text-label"><span>Python</span> <span class="shadow-text lang-badge py">PY</span></span></div>

<span class="mdc-tab-indicator"><span aria-hidden="true" class="mdc-tab-indicator__content mdc-tab-indicator__content--underline"></span></span></button></div>

</div>

</div>

</nav>

</div>

<div class="mt-2">

<div class="AnswerBody">

    public class Queue<T> where T : class
    {
        private Stack<T> input = new Stack<T>();
        private Stack<T> output = new Stack<T>();

        public void Enqueue(T t)
        {
            input.Push(t);
        }

        public T Dequeue()
        {
            if (output.Count == 0)
            {
                while (input.Count != 0)
                {
                    output.Push(input.Pop());
                }
            }

            return output.Pop();
        }
    }

</div>

</div>

</div>

<div class="row my-2">

<div><span>Source: <span>stackoverflow.com https://stackoverflow.com/questions/69192/how-to-implement-a-queue-using-two-stacks "Implement a Queue using two Stacks Interview Questions Source To Answer"</span></span>   </div>

</div>

</div>

</div>

</div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 7\. Implement Stack using Two Queues (with efficient push)

</div>

<div>

### Answer:

<div class="answer">

<div>

<div class="mb-2"><span class="h5">Problem</span></div>

<div>

<div class="AnswerBody">

Given two queues with their standard operations (`enqueue`, `dequeue`, `isempty`, `size`), implement a stack with its standard operations (`pop`, `push`, `isempty`, `size`). The stack should be efficient when pushing an item.

</div>

</div>

<div>

<div class="AnswerBody">

Given we have `queue1` and `queue2`:

**push** - `O(1)`:

*   enqueue in `queue1`

**pop** - `O(n)`:

*   while size of `queue1` is bigger than 1, pipe (dequeue + enqueue) dequeued items from `queue1` into `queue2`
*   dequeue and return the last item of `queue1`, then switch the names of `queue1` and `queue2`

</div>

</div>

<div>

<div class="mb-2 mt-2"><span class="h5">Complexity Analysis</span></div>

<div class="hide-small">

<div class="row no-gutters my-2 align-items-end">

<div class="col font-weight-bold text-muted">Time:</div>

<div class="col text-center">

<div class="text-muted font-weight-bold justify-content-center">Constant</div>

<div class="complexity amazing first p-1 justify-content-center shadow-text selected-complexity effect7">O(1)</div>

</div>

<div class="col disable text-center">

<div class="text-muted font-weight-bold justify-content-center">Dbl. Logarithmic</div>

<div class="complexity good p-1 justify-content-center shadow-text">O(log log n)</div>

</div>

<div class="col disable text-center">

<div class="text-muted font-weight-bold justify-content-center">Logarithmic</div>

<div class="complexity good p-1 justify-content-center shadow-text">O(log n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold  text-muted justify-content-center">Square Root</div>

<div class="complexity fair p-1 justify-content-center shadow-text ">O(√n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold  text-muted justify-content-center">Linear</div>

<div class="complexity fair p-1 justify-content-center shadow-text ">O(n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold text-muted justify-content-center">Linearithmic</div>

<div class="complexity bad p-1 justify-content-center shadow-text ">O(n log n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold  text-muted justify-content-center">Quadratic</div>

<div class="complexity terrible p-1 justify-content-center shadow-text ">_O_(_n_<sup>2</sup>)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold   text-muted justify-content-center">Exponential</div>

<div class="complexity terrible p-1 justify-content-center shadow-text ">_O_(_2_<sup>n</sup>)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold text-muted">Factorial</div>

<div class="complexity terrible last p-1 justify-content-center shadow-text ">O(n!)</div>

</div>

</div>

</div>

<div class="hide-small">

<div class="row no-gutters my-2 align-items-end">

<div class="col font-weight-bold text-muted">Space:</div>

<div class="col text-center">

<div class="text-muted font-weight-bold justify-content-center">Constant</div>

<div class="complexity amazing first p-1 justify-content-center shadow-text selected-complexity effect7">O(1)</div>

</div>

<div class="col disable text-center">

<div class="text-muted font-weight-bold justify-content-center">Dbl. Logarithmic</div>

<div class="complexity good p-1 justify-content-center shadow-text">O(log log n)</div>

</div>

<div class="col disable text-center">

<div class="text-muted font-weight-bold justify-content-center">Logarithmic</div>

<div class="complexity good p-1 justify-content-center shadow-text">O(log n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold  text-muted justify-content-center">Square Root</div>

<div class="complexity fair p-1 justify-content-center shadow-text ">O(√n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold  text-muted justify-content-center">Linear</div>

<div class="complexity fair p-1 justify-content-center shadow-text ">O(n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold text-muted justify-content-center">Linearithmic</div>

<div class="complexity bad p-1 justify-content-center shadow-text ">O(n log n)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold   text-muted justify-content-center">Quadratic</div>

<div class="complexity terrible p-1 justify-content-center shadow-text ">_O_(_n_<sup>2</sup>)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold   text-muted justify-content-center">Exponential</div>

<div class="complexity terrible p-1 justify-content-center shadow-text ">_O_(_2_<sup>n</sup>)</div>

</div>

<div class="col disable text-center">

<div class="font-weight-bold text-muted">Factorial</div>

<div class="complexity terrible last p-1 justify-content-center shadow-text ">O(n!)</div>

</div>

</div>

</div>

<div class="hide-large">

**Time:** <mark>O(1)</mark>

**Space:** <mark>O(1)</mark>

</div>

<div class="mt-3">

<div>

<div class="AnswerBody">

If queue is implemented as _linked list_ the `enqueue` operation has `O(1)` time complexity.

</div>

</div>

</div>

</div>

<div style="font-size: 14px;">

<div class="mb-3 mt-2"><span class="h5">Implementation</span></div>

<div>

<nav class="mdc-tab-bar">

<div class="mdc-tab-scroller">

<div class="mdc-tab-scroller__scroll-area mdc-tab-scroller__scroll-area--scroll" style="margin-bottom: 0px;">

<div class="mdc-tab-scroller__scroll-content"><button class="mdc-ripple-upgraded mdc-ripple-upgraded--background-focused mdc-tab mdc-tab--min-width mdc-tab--active" aria-selected="true" tabindex="0">

<div class="mdc-tab__content"><span class="mdc-tab__text-label"><span>Java</span> <span class="shadow-text lang-badge java">Java</span></span></div>

<span class="mdc-tab-indicator mdc-tab-indicator--active"><span aria-hidden="true" class="mdc-tab-indicator__content mdc-tab-indicator__content--underline"></span></span></button></div>

</div>

</div>

</nav>

</div>

<div class="mt-2">

<div class="AnswerBody">

    public Stack<E> {
        private Queue<E> q1 = new Queue<E>();
        private Queue<E> q2 = new Queue<E>();

        public void push(E x) {
            q1.enqueue(x);
        }

        public E pop() {
            while (q1.size() > 1) {
                q2.enqueue(q1.dequeue());
            }
            E pop = q1.dequeue();
            Queue<E> temp = q1;
            q1 = q2;
            q2 = temp;
            return pop;
        }
    }

</div>

</div>

</div>

<div class="row my-2">

<div><span>Source: <span>stackoverflow.com https://stackoverflow.com/questions/688276/implement-stack-using-two-queues "Implement Stack using Two Queues (with efficient `push`) Interview Questions Source To Answer"</span></span>   </div>

</div>

</div>

</div>

</div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 8\. Name some Queue implementations and compare them by efficiency of operations

</div>

<div>👉🏼 Check all 14 answers https://devinterview.io/data/queues-interview-questions </div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 9\. What are benefits of Circular Queue?

</div>

<div>👉🏼 Check all 14 answers https://devinterview.io/data/queues-interview-questions </div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 10\. Compare Array-Based vs List-Based implementation of Queues

</div>

<div>👉🏼 Check all 14 answers https://devinterview.io/data/queues-interview-questions </div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 11\. How to manage Full Circular Queue event?

</div>

<div>👉🏼 Check all 14 answers https://devinterview.io/data/queues-interview-questions </div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 12\. Name most efficient way to implement Stack and Queue together?

</div>

<div>👉🏼 Check all 14 answers https://devinterview.io/data/queues-interview-questions </div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 13\. How do I convert a Queue into the Stack?

</div>

<div>👉🏼 Check all 14 answers https://devinterview.io/data/queues-interview-questions </div>

</div>

<div data-v-5e9078c0="" class="unit">

<div>

## 🔹 14\. How implement a Queue using only One (1) Stack?

</div>

<div>👉🏼 Check all 14 answers https://devinterview.io/data/queues-interview-questions </div>

</div>

Thanks 🙌 for reading and good luck on your next tech interview!  
Explore 3800+ dev interview question here 👉 [Devinterview.io https://devinterview.io/)</div>
