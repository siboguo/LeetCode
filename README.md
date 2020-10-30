<!-- GFM-TOC -->
* [MonotonicQueue](#MonotonicQueue)
<!-- GFM-TOC -->

# MonotonicQueuq
A monotonic Queue is a data structure the elements from the front to the end is strictly either increasing or decreasing

# Code
public class MonotonicQueue
	{
		public static LinkedList<int> list = new LinkedList<int>();
		//在队尾添加元素 n
		public void Push(int n)
		{
			while(list.Count>0 && list.Last.Value < n)
			{
				list.RemoveLast();
			}
			list.AddLast(n);
		}
// 返回当前队列中的最大值
		public int Max()
		{
			return list.First.Value;
		}
// 队头元素如果是 n，删除它
		public void Pop(int n)
		{
			if(list.First.Value==n)
				list.RemoveFirst();
		}
	}
