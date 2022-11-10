# He
additional
```
#include <iostream>
using namespace std;

int main()
{
	int n, m;
	int a[10], b[10];
	cin >> n >> m;
	for (int i = 0; i < n; ++i)
	{
		cin >> a[i];
	}

	for (int i = 0; i < m; ++i)
	{
		cin >> b[i];
	}

	int c[10];
	int cs[10];
	int k = 0;

	for (int i = 0; i < n; ++i)
	{
		int flag = 1;
		for (int j = 0; j < m; ++j)
		{
			if (a[i] == b[j])
			{
				flag = 0;
				break;
			}
		}
		if (flag == 1)
		{
			if (k == 0)
			{
				c[k] = a[i];
				cs[k] = a[i];
				k++;
			}
			else
			{
				c[k] = a[i];
				cs[k] = a[i];
				int flag1 = 1;
				for (int t = 0; t < k; ++t)
				{
					if (c[k] == cs[t])
					{
						break;
					}
				}
				if (flag1 == 1)
				{
					c[k] = a[i];
					cs[k] = a[i];
					k++;
				}
			}
		}
	}

	int d[10];
	int ds[10];
	int l = 0;
	for (int j = 0; j < m; j++)
	{
		int flag2 = 1;
		for (int i = 0; i < n; ++i)
		{
			if (b[j] == a[i])
			{
				flag2 = 0;
				break;
			}
		}
		if (flag2 == 1)
		{
			if (l == 0)
			{
				d[l] = b[j];
				ds[l] = b[j];
				l++;
			}
			else
			{
				d[l] = b[j];
				ds[l] = b[j];
				int flag3 = 1;
				for (int t1 = 0; t1 < l; ++t1)
				{
					if (d[l] == ds[t1])
					{
						flag3 = 0;
					}
				}
				if (flag3 == 1)
				{
					d[l] = b[j];
					ds[l] = b[j];
					l++;
				}
			}
		}
	}
	cout << "不是这两个数组共有的元素为:" << endl;
	for (int i = 0; i < k; ++i)
	{
		cout << c[i] << ' ';
	}
	putchar('\n');

	for (int i = 0; i < l; ++i)
	{
		cout << d[i] << ' ';
	}
	return 0;
}
```
