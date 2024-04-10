# DSA-Middle-of-the-Linked-List
Given the head of a singly linked list, return the middle node of the linked list.

If there are two middle nodes, return the second middle node.

'''
Input: head = [1,2,3,4,5]
Output: [3,4,5]
Explanation: The middle node of the list is node 3.
'''
'''
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def middleNode(self, head: Optional[ListNode]) -> Optional[ListNode]:
        lenght=0
        dummy=ans=head
        while dummy: #Time cost O(n)
            dummy=dummy.next
            lenght+=1
        if lenght%2==0:
            k=lenght/2
        else:
            k=lenght//2
        for _ in range(int(k)): #Time cost O(m)
            ans=ans.next
        return ans # Space cost O(1)
    '''
    Total time cost O(n) + O(m) - while m is always <n then 2O(n) -> O(n)
    Total space cost O(1)
    '''
'''
