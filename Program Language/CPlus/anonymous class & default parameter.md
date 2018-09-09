```
#include "stdafx.h"

class TestCls
{
public:
    TestCls(int nId) :m_nId(nId) {};

    ~TestCls() {};
    
    int GetId()
    {
        return m_nId;
    }
private:
    int m_nId;
};

int foo(int a, TestCls test = TestCls(5))
{
    return a + test.GetId();
}

int main()
{
    printf("%d\n",foo(3));
    getchar();
    return 0;
}
```
