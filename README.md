# ManyToOne_OneToMany_Loop_Problem_Solved



@OneToMany(fetch = FetchType.LAZY, cascade = {CascadeType.REFRESH}, orphanRemoval = true, mappedBy = "house_id")
@JsonIgnoreProperties("house_id")
private List<Rooms> rooms = new ArrayList<Rooms>();

@ManyToOne(cascade= {CascadeType.MERGE})
@JoinColumn(name = "house_id", columnDefinition = "bigint", referencedColumnName = "id", nullable = false)
@JsonIgnoreProperties("rooms")
private House house_id;

//Generate The Getter and Setter 
// Do not override toString()
//no ---- @JsonIgnore Annotation in child Class.......
