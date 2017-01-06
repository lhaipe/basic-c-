# basic-c-
something unuseful
#include<iostream>
using namespace std;

class Complex
{
public:
Complex()
{
  m_real=0;
  m_imag=0;
}
Complex(int real,int imag)
{
  m_real=real;
  m_imag=imag;
}
Complex operator+(const Complex &t)
{
  return Complex(m_real+t.m_real,m_imag+t.m_imag);
}

~Complex()
{}
private:
  int m_real;
  int m_imag;
};

void main()
{
  Complex t1;
  Complex t2(10,20);
  Complex t3(30,40);
  Complex t4;
  t4=t2+t3;
}
