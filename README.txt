COMP 313/413 Project 2 Report Template

TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

		No there is no difference in the behavior.

TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

			This method removes the element at index 5 from the list, and shifts the rest of the list back.

		list.remove(Integer.valueOf(5)); // what does this one do?

			This method searches for the first occurrence of "5" in the list and, if it is present, removes it.

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

			This would result in the removal of the element at index 77 from the list.

TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.
	These are examples of SIZEs you might choose, you can choose others if you wish.

	SIZE 10
								  #1    #2    #3
        testArrayListAddRemove:  674ms 651ms 695ms
        testLinkedListAddRemove: 56ms  55ms  68ms
		testArrayListAccess:     33ms  41ms  52ms
        testLinkedListAccess:    26ms  27ms  28ms

	SIZE 100
								  #1    #2    #3
        testArrayListAddRemove:  682ms 779ms 417ms
        testLinkedListAddRemove: 69ms  63ms  74ms
		testArrayListAccess:     43ms  45ms  45ms
        testLinkedListAccess:    57ms  52ms  67ms

	SIZE 1000
								  #1     #2     #3
        testArrayListAddRemove:  1090ms 1041ms 950ms
        testLinkedListAddRemove: 65ms   55ms   60ms
		testArrayListAccess:     49ms   42ms   41ms
        testLinkedListAccess:    676ms  653ms  668ms

	SIZE 10000
								  #1     #2     #3
        testArrayListAddRemove:  3895ms 2767ms 2759ms
        testLinkedListAddRemove: 67ms   61ms   64ms
		testArrayListAccess:     45ms   42ms   67ms
        testLinkedListAccess:    9299ms 8051ms 7371ms

	listAccess - which type of List is better to use, and why?

		ArrayList is better to use for this because, as SIZE increases, the time it takes to execute the test stays consistent.
		The time to execute the test for the LinkedList option increases as SIZE increases, which is not an ideal time complexity.
		This is because ArrayList does not need to search through elements, whereas LinkedList does.

	listAddRemove - which type of List is better to use, and why?

		LinkedList is better to use for this because, as SIZE increases the time it takes to execute the test stays pretty consistent.
		The time to execute the test for the ArrayList option increases by a lot as SIZE increases.
		This is because LinkedList can add or remove nodes from the front of the list, but ArrayList has to shift elements, which takes longer.