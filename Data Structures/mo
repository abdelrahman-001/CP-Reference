const int sz = 320;
class query {
public:
    int l , r , id;
    query(int l1 , int r1 , int id1) {
        l = l1;
        r = r1;
        lvl = lvl1;
        id = id1;
    }
    bool operator < (const query &q) {
        return make_pair(l / sz , r) < make_pair(q.l / sz , q.r);
    }
};
void add(int x) {

}
void remove(int x) {

}
int get_ans(int lvl) {

}
vector<ll> mo_algo(vector<query> &v) {
    sort(v.begin() , v.end());
    vector<ll> q((int)v.size());
    int l = 1 , r = 0;
    for(auto &i:v) {
        int l1 = i.l , r1 = i.r;
        while(l1 < l)
            add(--l);
        while(r < r1)
            add(++r);
        while(l < l1)
            remove(l++);
        while(r1 < r)
            remove(r--);
        q[i.id] = get_ans();
    }
    return q;
}
int main() {
    vector<query>v;
    for(int i = 0;i < m;i++) {
        int l , r;
        cin >> l >> r;
        v.push_back(query(l , r , i));
    }
    vector<ll>ans = mo_algo(v);
    for(auto i:ans)
        cout << i << '\n';
}
