# ci-cd
1. git log --reverse --pretty=format:"%h %an %ae %ad %s" | head -n 1
349fdef michaelisvy misvy@vmware.com Wed Jan 9 01:05:18 2013 -0800 Initial commit
2. git branch -r | wc -l
9
3. git shortlog -s -n

   210  Mic
   151  Dave Syer
   136  Antoine Rey
4.  git tag | wc -l   

       1
    git tag

        1.5.x
    git show 1.5.x     
        commit c36452a2c34443ae26b4ecbba4f149906af14717 (tag: 1.5.x)
        Author: Dave Syer <dsyer@pivotal.io>
        Date:   Fri Nov 3 14:17:04 2017 +0000

            Use leading / in app URL
            
            Fixes gh-267

        diff --git a/src/main/resources/templates/owners/ownersList.html b/src/main/resources/templates/owners/ownersList.html
        index dc4c446..478b37e 100644
        --- a/src/main/resources/templates/owners/ownersList.html
        +++ b/src/main/resources/templates/owners/ownersList.html
        @@ -19,7 +19,7 @@
                <tbody>
                <tr th:each="owner : ${selections}">
                    <td>
        -                  <a th:href="@{owners/__${owner.id}__}" th:text="${owner.firstName + ' ' + owner.lastName}"/></a>
        +                  <a th:href="@{/owners/__${owner.id}__}" th:text="${owner.firstName + ' ' + owner.lastName}"/></a>
                    </td>
                    <td th:text="${owner.address}"/>
                    <td th:text="${owner.city}"/>
5. git remote -v

origin	https://github.com/spring-projects/spring-petclinic (fetch)
origin	https://github.com/spring-projects/spring-petclinic (push)