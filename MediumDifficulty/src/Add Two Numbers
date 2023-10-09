/** 2. Add Two Numbers
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
        // Create a dummy node to serve as the head of the result list.
        ListNode dummyHead = new ListNode(0); 
        // Initialize a current node to traverse the result list.
        ListNode current = dummyHead; 
        // Initialize a carry variable to handle any carry-over from addition.

        while (l1 != null || l2 != null) {
            // Get the values of the current nodes in l1 and l2 (or 0 if null).
            int x = (l1 != null) ? l1.val : 0;
            int y = (l2 != null) ? l2.val : 0; 
            // Calculate the sum of the current digits along with the carry.
            int sum = carry + x + y; 
            // Calculate the carry for the next iteration.
            carry = sum / 10;
            // Create a new node with the sum's digit and add it to the result list.
            current.next = new ListNode(sum % 10); 
            // Move the current pointer to the newly added node.

            // Move to the next nodes in l1 and l2 if they exist.
            if (l1 != null) l1 = l1.next; 
            if (l2 != null) l2 = l2.next; 
        }

        // If there is a carry left after the loop, create a new node for it.
        if (carry > 0) {
            current.next = new ListNode(carry); 
        }

        // Return the result list starting from the node after the dummy head.
        return dummyHead.next; 
    }
}
