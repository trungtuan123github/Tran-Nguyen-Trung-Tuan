# Tran-Nguyen-Trung-Tuan
dovote what you can do
#include<iostream>
using namespace std;
int main() 
{
	int date, month, year,t,hople,th,s;
	cout << "date:";
	cin >> date;
	cout << "\nmonth:";
	cin >> month;
	cout << "\nyear :";
	cin >> year;
	if ((year % 400 == 0) || (year % 4 == 0 && !(year % 100 == 0)))
	{

		t = 1;
		if (month < 13)
		{
			if (month == 2)
			{

				if (date > 29)
				{
					hople = 0;
				}
				else
				{
					hople = 1;
					th = 1;
					//cout << "\nthang 2 co 29 ngay\n";
				}

			}
			else
			{
				if (month == 4 || month == 6 || month == 9 || month == 11)
				{
					if (date > 30)
					{
						hople = 0;
					}
					else
					{
						hople = 1;
						//cout << "thang " << month << " co 30 ngay";
						th = 3;
					}

				}
				else
				{
					if (date > 31)
					{
						hople = 0;
					}
					else
					{
						hople = 1;
						//cout << "thang " << month << " co 31 ngay";
						th = 4;
					}

				}
			}
		}
		else
			hople = 0;
	}
	else
	{
		t = 0;
		if (month < 13)
		{
			if (month == 2)
			{

				if (date > 28)
				{
					hople = 0;
				}
				else
				{
					hople = 1;
					th = 2;
					//cout << "\nthang 2 co 28 ngay\n";
				}

			}
			else
			{
				if (month == 4 || month == 6 || month == 9 || month == 11)
				{
					if (date > 30)
					{
						hople = 0;
					}
					else
					{
						hople = 1;
						//cout << "thang " << month << " co 30 ngay";
						th = 3;
					}

				}
				else
				{
					if (date > 31)
					{
						hople = 0;
					}
					else
					{
						hople = 1;
						//cout << "thang " << month << " co 31 ngay";
						th = 4;
					}

				}
			}

		}
		else
		{
			hople = 0;

		}
		
	};
	if (hople == 1)
	{
		cout << "\ndu lieu ngay thang hop le\n";
		if (t == 1)
		{
			cout << year << " \nla nam nhuan va co 366 ngay\n";
		}

		else { cout << year << " \nla nam khong nhuan va co 365 ngay\n"; };
		switch (th)
		{
		case 1:
			cout << "\nthang 2 co 29 ngay\n";
			break;
		case 2:
			cout << "\nthang 2 co 28 ngay\n";
			break;
		case 3:
			cout << "\nthang " << month << " co 30 ngay\n";
			break;
		default:
			cout << "\nthang " << month << " co 31 ngay\n";
		}
		s = 0;
		if (month==1)
		{
			s = date;
			
		}
		else
		{
			for (int i = 1; i < month; i++)
			{
				switch (i)
				{
				case 1:
					s = s + 31;
					break;
				case 2:
					if (t == 1)
						s = s + 29;
					if (t == 0)
						s = s + 28;
					break;
				case 3:
						s = s + 31;
						break;
				case 4:
					s = s + 30;
					break;
				case 5:
					s = s + 31;
					break;
				case 6:
					s = s + 30;
					break;
				case 7:
					s = s + 31;
					break;
				case 8:
					s = s + 31;
					break;
				case 9:
					s = s + 30;
					break;
				case 10:
					s = s + 31;
					break;
				case 11:
					s = s + 30;
	



				}
				
			};
			s = s + date;
		}
		
		cout << "hom nay la ngay thu " << s << " trong nam " << year << endl;

	}
	else
	{
		cout << "\ndu lieu khong hop le\n";
	};
	system("pause");
	return 0;
}
