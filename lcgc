#include <iostream>
#include <vector>
using namespace std;

vector <int> g;

void fad(int u_) //finding all divisors (fad)
{
    for (int i = 1; i <= 65535; i++)
        if (u_ % i == 0)
        {
            g.push_back(i);
        }
}

int main() {
    int mass[4];
    int t[3];
    int u_;
    vector <int> a_pos;
    bool f = false;

    cout << "\n-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-\n";
    cout << "\nEnter 4 numbers:";
    cin >> mass[0] >> mass[1] >> mass[2] >> mass[3];

    //Example:
    // 5054 25789 13214 16605


    //Search for the maximum value of the number "m"
    t[0] = mass[1] - mass[0];
    t[1] = mass[2] - mass[1];
    t[2] = mass[3] - mass[2];
    u_ = abs(t[2] * t[0] - t[1] * t[1]);
    cout << "\n-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-\n";
    cout << "\nThe maximum size of the number \"m\" is " << u_ << ";\n";
    cout << "\n-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-\n";

    //Search for all divisors of the number "m"
    fad(u_);

    //Search for possible values of the number "a" according to the remainder when dividing
    for (int u : g) {
        for (int i = 0; i <= u; i++) {
            int z = ((i * i * t[0]) % u);
            if (z < 0) {
                z = u + z;
            }
            int t_2;
            if (t[2] < 0) {
                t_2 = t[2] + u;
            }
            else {
                t_2 = t[2];
                }
            if (z == t_2) {
                a_pos.push_back(i);
            }
        }

        //Iterating through all the values for the number "b"
        for (int a_po : a_pos) {
            for (int j = 0; j <= u; j++) {
                if (((mass[0] * a_po + j) % u) == mass[1] && ((mass[1] * a_po + j) % u) == mass[2] &&
                    ((mass[2] * a_po + j) % u) == mass[3]) {
                    cout << "\n\"m\" can be " << u << ", \"a\" can be " << a_po << ", \"b\" can be " << j << ", so";
                    cout << "\n\"x5\" can be " << (mass[3] * a_po + j) % u << "\n";
                    cout << "\n-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-\n";
                    f = true;
                    break;
                }
            }
        }
    }
    if (!f) {
        cout << "\n***************************************\n";
        cout << "\n! ERROR: these numbers do not form a Linear Congruent Sequence (LCS)\n";
        cout << "\n***************************************\n";
    }
    else {
        cout << "\n***************************************\n";
        cout << "\nAbove are examples of how these numbers can form a Linear Congruent Sequence (LCG)\n";
        cout << "\n***************************************\n";
    }
}
