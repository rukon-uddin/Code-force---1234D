#include<bits/stdc++.h>
using namespace std;
int main()
{
    vector<set<int>>position(26);
    string str;
    cin>>str;
    int len = (int)str.size();
    for(int i=0;i<len;i++)
    {
        position[str[i]-'a'].insert(i);
    }
    int n;
    cin>>n;
    for(int i=0; i<n; i++)
    {
        int q;
        cin>>q;
        if(q==1)
        {
            int pos;
            char ch;
            cin>>pos>>ch;
            --pos;
            position[str[pos] - 'a'].erase(pos);
            str[pos] = ch;
            position[str[pos] - 'a'].insert(pos);
        }else
        {
            int l,r;
            cin>>l>>r;
            --l;--r;
            int cnt = 0;
            for(int i=0; i<26; i++)
            {
                auto it = position[i].lower_bound(l);
                if(it!=position[i].end() && *it<=r)
                {
                    cnt++;
                }
            }
            cout<<cnt<<"\n";
        }
    }
    return 0;

}

