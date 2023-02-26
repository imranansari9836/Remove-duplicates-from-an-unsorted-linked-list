class Solution
{
    //Function to remove duplicates from unsorted linked list.
    public Node removeDuplicates(Node head) 
    {
        Node curr=head;//5
        HashSet<Integer>set=new HashSet<>();
        while(curr.next!=null)
        {
            set.add(curr.data);
            if(set.contains(curr.next.data))
            {
                curr.next=curr.next.next;
            }
            else
            {
                curr=curr.next;//2
            }
        }
        return head;//5 2 4
    }
}
