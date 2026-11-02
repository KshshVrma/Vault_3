class PrefixSum2D {
    vector<vector<int>> prefix;

public:

    PrefixSum2D(vector<vector<int>>& matrix) {

        int n = matrix.size();
        int m = matrix[0].size();

        prefix.assign(n + 1, vector<int>(m + 1, 0));

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= m; j++) {

                prefix[i][j] =
                    matrix[i-1][j-1]
                    + prefix[i-1][j]
                    + prefix[i][j-1]
                    - prefix[i-1][j-1];
            }
        }
    }

    int query(int r1, int c1, int r2, int c2) {

        return prefix[r2+1][c2+1]
             - prefix[r1][c2+1]
             - prefix[r2+1][c1]
             + prefix[r1][c1];
    }
};

to calculate sum of any rectangle value in o1 time