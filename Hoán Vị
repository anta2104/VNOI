#include <bits/stdc++.h>

using namespace std;

typedef long long ll;

const ll MOD = 1e9 + 7;
const int N = 3002;

int n;
ll f[N][N];
string s;

int main() {
    cin >> n;
    f[1][1] = 1;
    for (int i = 2; i <= n; ++i) {
        char ch;
        cin >> ch;
        for (int j = 1; j <= i; ++j) {
            if (ch == '<') {
                f[i][j] = f[i - 1][j - 1];
            } else {
                f[i][j] = (f[i - 1][i - 1] + MOD - f[i - 1][j - 1]) % MOD;
            }
        }
        for (int j = 1; j <= i; ++j)
            (f[i][j] += f[i][j - 1]) %= MOD;
    }
    cout << f[n][n] << "\n";
    return 0;
}
