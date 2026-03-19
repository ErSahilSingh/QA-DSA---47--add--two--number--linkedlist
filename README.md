# QA-DSA---47--add--two--number--linkedlist

var addTwoNumbers = function(l1, l2) {

    let ans= new ListNode(0)
    let anshead =ans
    let carry =0
    while(l1 || l2 || carry){
        let val1 = l1 ? l1.val : 0;
        let val2 = l2 ? l2.val : 0;
        let sum = val1 + val2 + carry;

        carry= Math.floor(sum/10)
        let digit= sum%10 
    
        let newnode= new ListNode(digit)
        ans.next=newnode
        ans=ans.next

        l1=l1 && l1.next
        l2=l2 && l2.next
    }

    return anshead.next
    
};
