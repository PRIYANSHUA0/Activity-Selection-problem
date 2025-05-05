# Activity-Selection-problem
activity selection problem using C++ 


    for (int i = 0; i < size; i++) {
        v.push_back({s[i], f[i]});
    }

    sort(v.begin(), v.end(), comp);

    int count = 1; 
    int lastFinish = v[0].second;

    for (int i = 1; i < size; i++) {
        if (v[i].first >= lastFinish) {
            count++;
            lastFinish = v[i].second;
        }
    }

    cout << "Total activities selected: " << count << endl;
    return count;
}
