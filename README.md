# LeetCode
#MonotonicQueue
class MonotonicQueue {
    // 在队尾添加元素 n
    void push(int n);
    // 返回当前队列中的最大值
    int max();
    // 队头元素如果是 n，删除它
    void pop(int n);
}
code
public class MonotonicQueue
	{
		public static LinkedList<int> list = new LinkedList<int>();
		
		public void Push(int n)
		{
			while(list.Count>0 && list.Last.Value < n)
			{
				list.RemoveLast();
			}
			list.AddLast(n);
		}

		public int Max()
		{
			return list.First.Value;
		}

		public void Pop(int n)
		{
			if(list.First.Value==n)
				list.RemoveFirst();
		}
	}
