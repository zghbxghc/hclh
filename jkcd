#include<cstdio>
#include<queue>
using namespace std;
const int maxn=100;
struct node
{
    int x,y;
    int step;
}Node;
int n,m;
int matrix[maxn][maxn];
bool inq[maxn][maxn]={false};
int X[4]={0,0,1,-1};
int Y[4]={1,-1,0,0};

bool judge(int x,int y)
{
    if(x>=n||x<0||y>=m||y<0)
        return false;
    if(matrix[x][y]==0||inq[x][y]==true)
        return false;
    return true;
}
void DFS(int x,int y)
{
    int dr,dx;
    if(x<0||x>=n||y<0||y>=m)
        return;
    if(matrix[x][y]!=1||inq[x][y]!=false)
        return;
    if(x==4&&y==3)
        return;
    inq[x][y]=true;
    DFS(x,y+1);
    DFS(x,y-1);
    DFS(x+1,y);
    DFS(x-1,y);
    }
    int main()
    {
        scanf("%d%d",&n,&m);
        for(int x=0;x<n;x++)
            for(int y=0;y<m;y++)
                scanf("%d",&matrix[x][y]);
        int ans=0;
        for(int x=0;x<n;x++)
            for(int y=0;y<m;y++)
                if(matrix[x][y]==1&&inq[x][y]==false)
                {
                    ans++;
                    DFS(x,y);
                }
                printf("%d",ans);
    }

