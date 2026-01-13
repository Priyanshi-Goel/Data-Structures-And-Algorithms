// A STRING OF INTEGER (ATOI)
// the problem desciption : 
// code as follows //
class Solution {
public:
    int myAtoi(string s) {
        long long ans = 0;
        int l = s.length();
        int i = 0;
        bool neg = false;
        while (i < l && s[i] == ' ')
            i++;
        if (s[i] == '-') {
            neg = true;
            i++;
        } else if (s[i] == '+')
            i++;
        while (i < l && (s[i] == '0'))
            i++;

        while (i < l) {
            if (!isdigit(s[i]))
                return ans;
            if (neg) {
                ans = ans * 10 - (s[i] - '0');
                if(ans<INT_MIN) return INT_MIN;
            } else {
                ans = ans * 10 + (s[i] - '0');
                if(ans>INT_MAX) return INT_MAX;

            }
            i++;
        }

        return ans;
    }
};
// approach and the thought processc//
/* we checked for some particular constraints i.e. 
   1. leading spaces and zeroes
   2. any sign +,-
   3. overflow or inflow conditions
   4. does string char isdigit or not
   5. once the digits start (including leadig 0) afterwards anyother char apart from digit even if it is +,- or whitespace will end and return the so far formed number ot of string
   we wrote logic according to these bullet points and returned the ans! */
