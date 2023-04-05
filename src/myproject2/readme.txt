gradeContent;
    }

    public static Comparator<CommentPlus062> GRADE062_COMPARATOR = (c1, c2) -> c1.grade062.compareTo(c2.grade062);

    public static Predicate<CommentPlus062> match062(Grade062 grade) {
        return (c) -> c.grade062 == grade;
    }
}
