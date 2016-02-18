//84104971101048411497 - Can you guess what does this mean?
using namespace std;
#include <bits/stdc++.h>
#define mapii map<int, int>
#define debug(a) cout << #a << ": " << a << endl
#define debuga1(a, l, r) fto(i, l, r) cout << a[i] << " "; cout << endl
#define fdto(i, r, l) for(int i = (r); i >= (l); --i)
#define fto(i, l, r) for(int i = (l); i <= (r); ++i)
#define forit(it, var) for(__typeof(var.begin()) it = var.begin(); it != var.end(); it++)
#define fordit(rit, var) for(__typeof(var.rbegin()) rit = var.rbegin(); rit != var.rend(); rit++)
#define ii pair<int, int>
#define iii pair<int, ii>
#define ff first
#define ss second
#define mp make_pair
#define pb push_back
#define ll long long
#define maxN 1005

int n, k, a[maxN][maxN];
ll f[maxN][maxN];

void Subtask1() {
    ll ans = 0;
    fto(x1, 1, n-k+1) {
        fto(y1, 1, n-k+1) {
            int x2 = x1+k-1, y2 = y1+k-1;
            ll sum = 0;
            fto(i, x1, x2) {
                fto(j, y1, y2) sum += a[i][j];
            }
            ans = max(ans, sum);
        }
    }
    cout << ans;
}

void Subtask2() {
    fto(i, 1, n) {
        fto(j, 1, n) f[i][j] = f[i-1][j]+f[i][j-1]-f[i-1][j-1]+a[i][j];
    }
    ll ans = 0;
    fto(x1, 1, n-k+1) {
        fto(y1, 1, n-k+1) {
            int x2 = x1+k-1, y2 = y1+k-1;
            ans = max(ans, f[x2][y2]-f[x2][y1-1]-f[x1-1][y2]+f[x1-1][y1-1]);
        }
    }
    cout << ans;
}

int main () {
    #ifndef ONLINE_JUDGE
        freopen("input.txt", "r", stdin);
        //freopen("output.txt", "w", stdout);
    #endif // ONLINE_JUDGE

    scanf("%d%d", &n, &k);
    fto(i, 1, n) {
        fto(j, 1, n) scanf("%d", &a[i][j]);
    }

    //Subtask1();
    Subtask2();

    return 0;
}
